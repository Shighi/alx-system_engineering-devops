# AirBnB Clone v2 - Web Framework Deployment

## Author: SHIGHI

This project focuses on deploying the AirBnB Clone v2 application using Flask, Gunicorn, and Nginx.

---

## Tasks Overview

### 0. Set up Development with Python

This task involves setting up a development environment to serve the AirBnB Clone v2 application on `web-01`.

#### Steps:
1. Ensure task #3 of your SSH project is completed for `web-01`.
2. Install `net-tools` package:
   ```bash
   sudo apt install -y net-tools
   ```
3. Clone the repository on `web-01`:
   ```bash
   git clone https://github.com/Shighi/alx-system_engineering-devops.git
   ```
4. Modify `web_flask/0-hello_route.py` to serve content from `/airbnb-onepage/` on port `5000`.
5. Ensure the Flask application object is named `app`.
6. Run the application:
   ```bash
   python3 -m web_flask.0-hello_route
   ```
7. Test with `curl`:
   ```bash
   curl 127.0.0.1:5000/airbnb-onepage/
   ```

---

### 1. Set up Production with Gunicorn

This task involves setting up a production environment using Gunicorn.

#### Steps:
1. Install Gunicorn:
   ```bash
   pip install gunicorn
   ```
2. Start Gunicorn with the application:
   ```bash
   gunicorn --bind 0.0.0.0:5000 web_flask.0-hello_route:app
   ```
3. Ensure nothing is listening on port `6000` before testing.
4. Test with `curl`:
   ```bash
   curl 127.0.0.1:5000/airbnb-onepage/
   ```

---

### 2. Serve a Page with Nginx

This task involves configuring Nginx to serve the application.

#### Steps:
1. Configure Nginx to serve the page from `/airbnb-onepage/`.
2. Proxy requests from Nginx to the application listening on port `5000`.
3. Include the Nginx config file as `2-app_server-nginx_config`.
4. Restart Nginx:
   ```bash
   sudo systemctl restart nginx
   ```
5. Test locally and publicly:
   ```bash
   curl 127.0.0.1/airbnb-onepage/
   curl YOUR_PUBLIC_IP/airbnb-onepage/
   ```

---

### 3. Add a Route with Query Parameters

This task involves configuring Nginx to proxy requests to a different Gunicorn instance for dynamic content.

#### Steps:
1. Modify `web_flask/6-number_odd_or_even.py` to serve at `/number_odd_or_even/<int:n>`.
2. Start a Gunicorn instance on port `5001`:
   ```bash
   tmux new-session -d 'gunicorn --bind 0.0.0.0:5001 web_flask.6-number_odd_or_even:app'
   ```
3. Update Nginx to proxy requests from `/airbnb-dynamic/number_odd_or_even/(any integer)` to `5001`.
4. Include the Nginx config file as `3-app_server-nginx_config`.
5. Restart Nginx:
   ```bash
   sudo systemctl restart nginx
   ```
6. Test:
   ```bash
   curl YOUR_PUBLIC_IP/airbnb-dynamic/number_odd_or_even/5
   ```

---

## Repository Structure

```
alx-system_engineering-devops/
├── 0x1A-application_server/
│   ├── 2-app_server-nginx_config
│   ├── 3-app_server-nginx_config
│   ├── web_flask/
│   │   ├── 0-hello_route.py
│   │   ├── 6-number_odd_or_even.py
│   ├── README.md
```


