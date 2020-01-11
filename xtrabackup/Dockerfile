FROM debian:stretch

COPY percona-xtrabackup-80_8.0.9-1.stretch_amd64.deb /tmp/percona-xtrabackup.deb
RUN apt-get update && apt-get -y install nmap \
	&& dpkg -i /tmp/percona-xtrabackup.deb && rm -Rf /tmp/percona-xtrabackup.deb \
	&& rm -rf /var/lib/apt/lists/*

# COPY entrypoint /usr/local/bin/entrypoint
# RUN chmod +x /usr/local/bin/entrypoint
# ENTRYPOINT ["/usr/local/bin/entrypoint"]