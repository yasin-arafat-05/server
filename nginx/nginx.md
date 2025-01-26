<br>
<br>

# `#Nginx:`

<br>

### [documentation_link](https://nginx.org/en/)

<br>

<br>
<br>

# `#01 Basic Information: `

<br>

### **Nginx-এর ব্যবহার এবং ভূমিকা**  

Nginx বহুমুখী একটি সার্ভার সফটওয়্যার। এটি বিভিন্ন উদ্দেশ্যে ব্যবহার করা যায়, যেমন:  

#### **1. ওয়েব সার্ভার:**  
Nginx একটি HTTP ওয়েব সার্ভার হিসেবে কাজ করে।  
- এটি ওয়েবসাইটের জন্য ডেটা পরিবেশন করে, যেমন HTML, CSS, JavaScript ফাইল।  
- ওয়েব ব্রাউজার থেকে ক্লায়েন্ট অনুরোধ গ্রহণ করে এবং সেগুলোর জন্য সঠিক ফাইল সরবরাহ করে।  

#### **2. রিভার্স প্রক্সি (Reverse Proxy):**  
রিভার্স প্রক্সি হলো একটি মাধ্যম যা ক্লায়েন্টের অনুরোধগুলোকে ব্যাকএন্ড সার্ভারে ফরওয়ার্ড করে।  
- এটি সার্ভারের আসল আইপি ঠিকানা গোপন রাখে এবং সার্ভারের সুরক্ষা বাড়ায়।  
- Nginx ক্লায়েন্ট এবং ব্যাকএন্ড সার্ভারের মধ্যে একটি মধ্যস্থতাকারী হিসেবে কাজ করে।  

#### **3. লোড ব্যালেন্সার (Load Balancer):**  
লোড ব্যালান্সার একাধিক সার্ভারের মধ্যে ক্লায়েন্টের অনুরোধ বিতরণ করে।  
- এটি সার্ভারের লোড কমায় এবং সার্ভিস ডাউন হওয়ার ঝুঁকি হ্রাস করে।  
- Nginx সহজেই সার্ভার ক্লাস্টার তৈরি করে এবং ট্র্যাফিক পরিচালনা করে।  

#### **4. ক্যাশিং (Caching):**  
ক্যাশিং হলো তথ্য বা ডেটা সাময়িকভাবে সংরক্ষণ করা, যাতে ভবিষ্যতে অনুরোধের জন্য দ্রুত সরবরাহ করা যায়।  
- Nginx আগের অনুরোধগুলোর ফলাফল ক্যাশ করে, ফলে সার্ভার দ্রুত কাজ করতে পারে।  
- উদাহরণ: যদি একজন ব্যবহারকারী বারবার একই পেজ অ্যাক্সেস করেন, ক্যাশিংয়ের কারণে সার্ভার নতুন করে ডেটা তৈরি না করেই পেজটি দেখাতে পারে।  

#### **5. রেট লিমিটিং (Rate Limiting):**  
Nginx একটি নির্দিষ্ট সময়ে কতগুলি অনুরোধ গ্রহণ করা যাবে তা সীমিত করতে পারে।  
- এটি DDoS আক্রমণ থেকে সুরক্ষা দেয়।  
- অতিরিক্ত ট্রাফিক এড়িয়ে সার্ভারের স্থিতিশীলতা বজায় রাখে।  

#### **6. স্ট্যাটিক সাইট হোস্টিং (Hosting Static Sites):**  
Nginx HTML, CSS, এবং JS-এর মতো স্ট্যাটিক ফাইল সরবরাহের জন্য খুব কার্যকর।  
- এটি দ্রুত এবং কম রিসোর্স ব্যবহার করে স্ট্যাটিক সাইট হোস্ট করতে পারে।  

#### **7. একাধিক সাইট হোস্টিং (Hosting Multiple Sites):**  
Nginx "সার্ভার ব্লক" এর মাধ্যমে একই সার্ভারে একাধিক ডোমেন হোস্ট করতে পারে।  
- উদাহরণ: একই সার্ভারে `example.com` এবং `blog.example.com` একসঙ্গে চালানো সম্ভব।  

#### **8. গেটওয়ে (Gateway):**  
Nginx অ্যাপ্লিকেশন সার্ভারের জন্য একটি গেটওয়ে হিসেবে কাজ করে।  
- এটি বিভিন্ন অ্যাপ্লিকেশন বা ডেটাবেসের সাথে সংযোগ স্থাপন করতে সাহায্য করে।  


### **গুরুত্বপূর্ণ টার্মস**  

#### **ওয়েব সার্ভার (Web Server):**  
ওয়েব সার্ভার হলো এমন একটি সার্ভার যা HTTP প্রোটোকল ব্যবহার করে ব্রাউজারের জন্য ডেটা সরবরাহ করে।  
- উদাহরণ: Apache, Nginx।  

#### **ক্যাশিং (Caching):**  
ক্যাশিং হলো একটি প্রক্রিয়া যেখানে ডেটা সাময়িকভাবে সংরক্ষণ করা হয়, যাতে ভবিষ্যতের অনুরোধে দ্রুত সাড়া দেওয়া যায়।  
- উদাহরণ: ওয়েব পেজের HTML ক্যাশ করে রাখা।  

#### **লোড ব্যালেন্সিং (Load Balancing):**  
লোড ব্যালেন্সিং একাধিক সার্ভারের মধ্যে অনুরোধ বিতরণ করে।  
- এটি সার্ভারকে অতিরিক্ত চাপ থেকে রক্ষা করে এবং সেবা নিশ্চিত করে। For scaling we use load balancing.

#### **রিভার্স প্রক্সি (Reverse Proxy):**  
রিভার্স প্রক্সি হলো এমন একটি মাধ্যম যা ক্লায়েন্টের অনুরোধ গ্রহণ করে এবং ব্যাকএন্ড সার্ভারে পাঠায়।  
- এটি সার্ভারের সুরক্ষা এবং কর্মক্ষমতা উন্নত করে।  

#### **রেট লিমিটিং (Rate Limiting):**  
রেট লিমিটিং একটি কৌশল যেখানে নির্দিষ্ট সময়ে অনুরোধের সংখ্যা সীমিত করা হয়।  
- এটি অতিরিক্ত অনুরোধ এবং আক্রমণ প্রতিরোধে কার্যকর।  


### **Nginx এবং Uvicorn-এর তুলনা**  

Uvicorn হলো একটি ASGI (Asynchronous Server Gateway Interface) সার্ভার যা ডাইনামিক অ্যাপ্লিকেশন পরিবেশনে ব্যবহৃত হয়। কিন্তু এটি স্ট্যাটিক ফাইল সার্ভিং বা লোড ব্যালেন্সিং-এর মতো কাজের জন্য উপযুক্ত নয়। Nginx এই কাজগুলো দক্ষতার সাথে করতে পারে।  

<br>
<br>
<br>

# `#02 Installation: `

<br>

**1. Download:**
```bash
sudo pacman -S nginx
```

**2. See Status:**
```bash
sudo systemctl status nginx
```

**3.start service:**

```bash
sudo systemctl enable nginx
sudo systemctl start nginx
```

**4. Now run:**

`Now, localhost in a browser, we will see nginx server is up and running. `

<br>
<br>
<br>

# `#03 Welcome Page and Configuration File: `

<br>

`When we install the nginx server. Then in /etc/nginx folder created. Visit the folder. In the folder we will see files and fodler like below: `

nginx
----fastcgi.conf  
----fastcgi_params  
----koi-utf
----koi-win  
----mime.types  
----nginx.conf  
----scgi_params  
----uwsgi_params  
----win-utf

`nignx.conf is the entry point of nginx server. Okay, let's see what inside have inside it. `

```bash
❯ cat nginx.conf

#user http;
worker_processes  1;

#error_log  logs/error.log;
#error_log  logs/error.log  notice;
#error_log  logs/error.log  info;

#pid        logs/nginx.pid;


events {
    worker_connections  1024;
}


http {
    include       mime.types;
    default_type  application/octet-stream;

    #log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
    #                  '$status $body_bytes_sent "$http_referer" '
    #                  '"$http_user_agent" "$http_x_forwarded_for"';

    #access_log  logs/access.log  main;

    sendfile        on;
    #tcp_nopush     on;

    #keepalive_timeout  0;
    keepalive_timeout  65;

    #gzip  on;

    server {
        listen       80;
        server_name  localhost;

        #charset koi8-r;

        #access_log  logs/host.access.log  main;

        location / {
            root   /usr/share/nginx/html;
            index  index.html index.htm;
        }

        #error_page  404              /404.html;

        # redirect server error pages to the static page /50x.html
        #
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   /usr/share/nginx/html;
        }

        # proxy the PHP scripts to Apache listening on 127.0.0.1:80
        #
        #location ~ \.php$ {
        #    proxy_pass   http://127.0.0.1;
        #}

        # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
        #
        #location ~ \.php$ {
        #    root           html;
        #    fastcgi_pass   127.0.0.1:9000;
        #    fastcgi_index  index.php;
        #    fastcgi_param  SCRIPT_FILENAME  /scripts$fastcgi_script_name;
        #    include        fastcgi_params;
        #}

        # deny access to .htaccess files, if Apache's document root
        # concurs with nginx's one
        #
        #location ~ /\.ht {
        #    deny  all;
        #}
    }


    # another virtual host using mix of IP-, name-, and port-based configuration
    #
    #server {
    #    listen       8000;
    #    listen       somename:8080;
    #    server_name  somename  alias  another.alias;

    #    location / {
    #        root   html;
    #        index  index.html index.htm;
    #    }
    #}


    # HTTPS server
    #
    #server {
    #    listen       443 ssl;
    #    server_name  localhost;

    #    ssl_certificate      cert.pem;
    #    ssl_certificate_key  cert.key;

    #    ssl_session_cache    shared:SSL:1m;
    #    ssl_session_timeout  5m;

    #    ssl_ciphers  HIGH:!aNULL:!MD5;
    #    ssl_prefer_server_ciphers  on;

    #    location / {
    #        root   html;
    #        index  index.html index.htm;
    #    }
    #}

}
```

#### **1. Structure Overview (এক লাইন ব্যাখ্যা):**
- **events:** Worker connections কনফিগার করা হয়েছে।
- **http:** HTTP সার্ভারের জন্য ডিফল্ট সেটআপ এবং সেটিংস সংজ্ঞায়িত করা হয়েছে।
  - **server:** নির্দিষ্ট পোর্ট (৮০) এবং রুট ডিরেক্টরির মাধ্যমে HTTP অনুরোধ পরিচালনা করা হয়েছে।
    - **location /**: `/usr/share/nginx/html` ডিরেক্টরিতে থাকা `index.html` বা `index.htm` ফাইল পরিবেশন করা হয়েছে।
    - **error_page:** 500, 502, 503, এবং 504 ত্রুটি পৃষ্ঠাগুলিকে `/50x.html` এ রিডাইরেক্ট করা হয়েছে।
    - **location = /50x.html:** ত্রুটি পৃষ্ঠার জন্য রুট ডিরেক্টরি সংজ্ঞায়িত করা হয়েছে।


#### **2. Configurations Explained (বিস্তারিত ব্যাখ্যা):**

##### **1. Global Settings:**
```nginx
worker_processes  1; # let's change it to auto
```
- **ব্যাখ্যা:** 
  - সার্ভার একসাথে কতগুলো প্রক্রিয়া চালাবে তা নির্ধারণ করা হয়েছে। 
  - এখানে ১টি প্রক্রিয়া চালানো হবে।

##### **2. events:**
```nginx
events {
    worker_connections  1024;
}
```
- **ব্যাখ্যা:**
  - একেকটি worker প্রক্রিয়া (worker process) সর্বোচ্চ ১০২৪টি কানেকশন(মূলত ইউজারের রিকোয়েস্ট বোঝায়) পরিচালনা করতে পারবে।

##### **3. http:**
```nginx
http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile      on;
    keepalive_timeout  65;
}
```
- **ব্যাখ্যা:**
  - **mime.types:** ফাইল টাইপ শনাক্ত করার জন্য `mime.types` ইনক্লুড করা হয়েছে।
  - **default_type:** কোনো ফাইলের টাইপ শনাক্ত করা না গেলে `application/octet-stream` সেট করা হবে।
  - **sendfile:** ফাইল পরিবেশনে দ্রুততা আনতে `sendfile` চালু করা হয়েছে।
  - **keepalive_timeout:** কানেকশন লাইভ রাখার সময়সীমা ৬৫ সেকেন্ড নির্ধারণ করা হয়েছে।

---

##### **4. server:**
```nginx
server {
    listen       80;
    server_name  localhost;
    location / {
        root   /usr/share/nginx/html;
        index  index.html index.htm;
    }
    error_page   500 502 503 504  /50x.html;
    location = /50x.html {
        root   /usr/share/nginx/html;
    }
}
```
- **ব্যাখ্যা:**
  - **listen 80:** HTTP অনুরোধ পোর্ট ৮০-এ শোনা হবে।
  - **server_name localhost:** সার্ভারকে লোকালহোস্ট নাম দিয়ে চিহ্নিত করা হয়েছে।
  - **location /**: `/usr/share/nginx/html` ডিরেক্টরির `index.html` বা `index.htm` ফাইল ডিফল্ট রুট হিসেবে সেট করা হয়েছে।
  - **error_page 500...504:** নির্দিষ্ট ত্রুটি কোডগুলির জন্য `/50x.html` ফাইল পরিবেশন করা হবে।
  - **location = /50x.html:** `/50x.html` ফাইলের জন্য রুট ডিরেক্টরি `/usr/share/nginx/html`।

---

##### **5. Commented Sections (যা আনকমেন্ট করা হয়নি):**
- **PHP Proxy বা FastCGI সাপোর্ট:** 
  - PHP স্ক্রিপ্ট প্রক্সি করার বা FastCGI সার্ভারের মাধ্যমে চালানোর জন্য কিছু ব্লক কমেন্ট আকারে রাখা হয়েছে।
- **HTTPS server:** 
  - SSL এর মাধ্যমে সিকিউর কানেকশনের জন্য একটি সার্ভার ব্লক কমেন্ট আকারে রাখা হয়েছে।

---

#### **এই কনফিগারেশনের কাজ:** 
1. **HTTP সার্ভার:** পোর্ট ৮০-এ HTTP অনুরোধ গ্রহণ ও পরিবেশন করবে।
2. **Static Files:** `/usr/share/nginx/html` থেকে `index.html` ফাইল পরিবেশন করবে।
3. **Error Handling:** ত্রুটি কোডগুলোর জন্য `/50x.html` পৃষ্ঠায় রিডাইরেক্ট করবে।
4. **Worker Connections:** এক প্রক্রিয়া সর্বোচ্চ ১০২৪টি কানেকশন পরিচালনা করবে।
5. **Performance Optimization:** `sendfile` চালু এবং `keepalive_timeout` ৬৫ সেকেন্ড সেট করা হয়েছে।



<br>
<br>
<br>

# `#04 Change in Configuration File: `

<br>

After changing something in nginx configuration file. If we restart our nginx server then there will be some downtime. So, we'll not restart our nginx server.So, we can do the following step:

**1. 1st, we will change see what we change is right or not:**
```bash
sudo nginx -t
```
If everything is alright then we can reload our nginx server. `Remember, if we have got an error with the first command. After that if we will reload the nginx server . Then, our nginx server will be crushed and we will see downtime in our websites.`

**2. Reload nginx Server:**
```bash
sudo systemctl reload nginx 
```

