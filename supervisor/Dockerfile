FROM python:3
RUN pip install supervisor
RUN mkdir -p /etc/supervisor && mkdir -p /etc/supervisor/conf.d
COPY supervisord.conf /etc/supervisor/
entrypoint supervisord -c /etc/supervisor/supervisord.conf && tail -f /tmp/supervisord.log
RUN pip install jinja2 aiomysql aiohttp
RUN mkdir -p srv/awesome/log
COPY www /srv/awesome/www
COPY awesome.conf /srv/awesome/
RUN cp /srv/awesome/awesome.conf /etc/supervisor/conf.d