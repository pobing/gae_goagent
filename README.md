> 1. get gae_goagent
<pre>
git clone gae_goagent.git
</pre>
> 2.  appid change to yourself appid
<pre>  
   cd ../google_appengine/goagent/server/python
   vim app.yaml
</pre>
> 3. upload server
<pre>  
cd ../google_appengine/goagent/
sudo python appcfg.py update goAgent/server/python
</pre>  
> 4. proxy.ini type your appid
  <pre>cd ../google_appengine/goagent/
 vim  proxy.ini
</pre>
> 5. import crt
<pre>
sudo apt-get install libnss3-tools
certutil -d sql:$HOME/.pki/nssdb -A -t TC -n "goagent" -i /home//dong/google_appengine/goagent/local/CA.crt 
</pre>
