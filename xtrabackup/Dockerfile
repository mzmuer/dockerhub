FROM debian:stretch

COPY percona-xtrabackup-80_8.0.9-1.stretch_amd64.deb /tmp/percona-xtrabackup.deb
COPY mysql-community-client-core_8.0.18-1debian9_amd64.deb /tmp/mysql-client.deb
RUN apt-get update && apt-get -y install curl lsb-release \
	nmap libdbd-mysql-perl rsync libaio1 libev4 libcurl4-openssl-dev libncurses5 \
	&& dpkg -i /tmp/percona-xtrabackup.deb && dpkg -i /tmp/mysql-client.deb && rm -Rf /tmp/percona-xtrabackup.deb \
	&& rm -rf /var/lib/apt/lists/*