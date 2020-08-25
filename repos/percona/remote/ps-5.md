## `percona:ps-5`

```console
$ docker pull percona@sha256:34c453b0c796d184df0f5049c3ff47aa3d6c6db0b344c6170b5fef5bfb615ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:68dad5e2efeb6893e2d7d116a1eae144f2c641c17d00e7869397395590c91651
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197968054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb49da8a7d3c22eb92a4de93d43ede592bb5487ac89ad866211a4f9ef8d11a3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 18:39:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 10 Aug 2020 18:41:04 GMT
RUN groupdel input && groupadd -g 999 mysql
# Mon, 10 Aug 2020 18:41:05 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Mon, 10 Aug 2020 18:41:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable original release
# Tue, 25 Aug 2020 18:29:22 GMT
ENV PERCONA_VERSION=5.7.31-34.1.el7
# Tue, 25 Aug 2020 18:30:16 GMT
RUN set -ex;     yum install -y         Percona-Server-server-57-${PERCONA_VERSION}         Percona-Server-devel-57-${PERCONA_VERSION}         Percona-Server-tokudb-57-${PERCONA_VERSION}         Percona-Server-rocksdb-57-${PERCONA_VERSION}         jemalloc         openssl         which         policycoreutils;         yum clean all;     rm -rf /var/cache/yum /var/lib/mysql
# Tue, 25 Aug 2020 18:30:17 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 25 Aug 2020 18:30:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 25 Aug 2020 18:30:18 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Tue, 25 Aug 2020 18:30:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Aug 2020 18:30:18 GMT
USER mysql
# Tue, 25 Aug 2020 18:30:18 GMT
EXPOSE 3306
# Tue, 25 Aug 2020 18:30:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14bc3f760dd091dd563d2ef48f1147f72762a2b31109b475d8dcb60d351993a`  
		Last Modified: Mon, 10 Aug 2020 18:46:17 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd29505baaec9c24f65109881fc6c0d6d097e1d3973e08df81965f3d7bbdeef`  
		Last Modified: Mon, 10 Aug 2020 18:46:15 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35af5ab9a3507b90b1780d5c5f6f67c87bf9ab542ff82c91768593541302d95d`  
		Last Modified: Mon, 10 Aug 2020 18:46:16 GMT  
		Size: 6.5 MB (6520666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120071707bdce8a2c097ec51e0ba326faf19d324fe2344135d47a195382e7a3`  
		Last Modified: Tue, 25 Aug 2020 18:31:15 GMT  
		Size: 115.6 MB (115577656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d36714b45d31e2c0d3060533bb22b194773c2314f76087bcd85c7ce01680688`  
		Last Modified: Tue, 25 Aug 2020 18:30:56 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fd1024e5c88aa4f5f0ce9960f3c2c77fc1bd423cc2e240926b3d69c3bfdc58`  
		Last Modified: Tue, 25 Aug 2020 18:30:55 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
