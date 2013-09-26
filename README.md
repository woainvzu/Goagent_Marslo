Goagent_Marslo
==============

The configuration about Goagent and google_appengine

# Offical webiste
- [Google Appengine](https://developers.google.com/appengine/)
    - [Google App Engine SDK for Python](https://developers.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python)
- [Goagent](http://www.goagent.org/)
    - [Download](https://code.google.com/p/goagent/downloads/list)

# Install
- Download
<pre><code>$ wget http://googleappengine.googlecode.com/files/google_appengine_1.8.5.zip
$ wget https://goagent.googlecode.com/files/goagent-2.1.5.7z
</code></pre>
- Extract
<pre><code>$ unzip google_appengine_1.8.5.zip
$ 7zr e goagent-2.1.5.7z -ogoogle_appengine/goagent/
</code></pre>

# Configuration
- goagent/local/proxy.ini
    - appid = <YourID>
    - For example:
    <pre><code>[gae]
    appid = woainvzu
    </code></pre>
- goagent/server/python/app.yaml
    - application: <YourID>
    - For example:
    <pre><code>application: woainvzu
    </code></pre>
- Update configure
<pre><code>$ python appcfg.py update goagent/server/python/
</code></pre>

# Run Goagent
- Run in Terminal:
<pre><code>$ python <Path_to_GoogleAppEngine>/google_appengine/goagent/local/proxy.py
</code></pre>
- Run as command:
<pre><code>$ cat "python <Path_to_GoogleAppEngine>/google_appengine/goagent/local/proxy.py" > runProxy
$ chmod +x runProxy
$ sudo ln -s <PATH_TO_RUNPROXY>/runProxy /usr/bin/runProxy
$ runProxy
</code></pre>
- Or copy `Scripts/runProxy` to <SOME_PATH>
And use `ln -s`
