---
layout: post
title:  "Android Tips #1"
date:   2017-07-11 18:37:52 +0200
categories: Android
---
Android Tips#1 Services & AsyncTask -Part 1-

The difference between Services and AsyncTask.

AsyncTask :

AsyncTask is a class on the SDK for performing background operations and not overload the UI Thread. With this, you can load data from SQLITE, WebServices, or all short operations (a few seconds at the most).
All operations will be executed in the

{% highlight java%}
  doInBackground()
{% endhighlight %}

that will publish the results of your operation(s).

But, I need to update my UI after this operation, how can i do that ?

It is easy, AsyncTask provide also another method

{% highlight java%}
  onPostExecute()
{% endhighlight %}

that help you to update you UI.

How can I implement AsyncTask ?

For this example, I will take the case of a WebServices call.

First : Create a new Class on Android Studio.

{% highlight java%}
  public class MyAsyncTask extends AsyncTask<String[], Void, Object> {

  }
{% endhighlight %}

In this example
  {% highlight java%} String[]{% endhighlight %}
  correspond to an Array of String as Param,
  {% highlight java%} Void{% endhighlight %}
  the unit during the Progress and
  {% highlight java%} Object{% endhighlight %}
the type for the result of you operation.
It could be anything you want. I take three example.

There is four step for an AsyncTask
{% highlight java%}
1.  void onPreExecute()
{% endhighlight %}
This previous method allow you to update UI, and prepare the AsyncTask. . For being more user-friendly, you can for example display a ProgressBar that will be dismiss on the {% highlight java%}
  onPostExecute()
{% endhighlight %}

{% highlight java%}
2.  Object doInBackground()
{% endhighlight %}

This method will the main "Method". It is here you perform you long operation (few second at most), as fetching data from Internet. You have to use AsyncTask for fetching data, otherwise Android will throw an error because you are trying to do Network Operation on the main Thread.

{% highlight java%}
3.  void onProgressUpdate(Void... values)
{% endhighlight %}

This method will be call by the original method publishProgress.  You can update a percentage for in the progressBar.

{%highlight java%}
4. protected void onPostExecute(Object o)
{% endhighlight %}

And the last method, can allow you to publish result on the UI.


{%highlight java%}
protected void onPostExecute(Object o){
  // The result will be publish on a textView that was declared previously.
  textView.setText((String) o);
}
{% endhighlight %}

You can adapte, the three type for the AsyncTask as you want.
