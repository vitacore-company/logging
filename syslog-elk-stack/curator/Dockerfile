FROM python:3-alpine as curator

RUN pip install elasticsearch-curator

COPY ./curator.yml /etc/curator/
COPY ./actions.yml /etc/curator/
COPY ./periodic/daily/curator /etc/periodic/daily/curator

ENTRYPOINT ["crond", "-f"]
