* get gae_goagent
<pre>
git clone gae_goagent.git
</pre>
*  appid change to yourself appid
<pre>
   cd ../google_appengine/goagent/server/python
   vim app.yaml
</pre>
* upload server
<pre>  
cd ../google_appengine/goagent/
sudo python appcfg.py update goAgent/server/python
</pre>  
* proxy.ini type your appid
 <pre>
 cd ../google_appengine/goagent/
 vim  proxy.ini
</pre>
* import crt
<pre>
sudo apt-get install libnss3-tools
certutil -d sql:$HOME/.pki/nssdb -A -t TC -n "goagent" -i /home//dong/google_appengine/goagent/local/CA.crt 
</pre>
* start 
  <pre>
/usr/bin/python /home/dong/google_appengine/goagent/local/proxy.py 
</pre>
* auto run 
<pre>
    /usr/bin/python /home/dong/google_appengine/goagent/local/proxy.py >> goagent.sh
    vi /etc/rc.local :    
   su dong -s /home/dong/Desktop/goagent.sh
</pre>

