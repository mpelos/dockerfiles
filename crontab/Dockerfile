FROM ubuntu:16.04

# Install cron
RUN apt-get update && apt-get install -y cron && apt-get clean

# Create the log file to be able to run tail
RUN touch /var/log/cron.log

CMD { tail -f /var/log/cron.log & cron -f; }
