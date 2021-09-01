FROM python:3
RUN pip install supervisor
RUN mkdir -p /etc/supervisor && mkdir -p /etc/supervisor/conf.d
COPY supervisord.conf /etc/supervisor/
entrypoint supervisord -c /etc/supervisor/supervisord.conf && tail -f /tmp/supervisord.log