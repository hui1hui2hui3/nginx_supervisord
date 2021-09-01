FROM mysupervisor:0.1
RUN pip install jinja2 aiomysql aiohttp
RUN mkdir -p srv/awesome/log
COPY www /srv/awesome/www
COPY awesome.conf /srv/awesome/
RUN cp /srv/awesome/awesome.conf /etc/supervisor/conf.d