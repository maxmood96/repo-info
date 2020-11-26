## `percona:centos`

```console
$ docker pull percona@sha256:a7031b4a86da3e5dc757ca7a75c4db22dc359a9fe8e54cd2c3c26805c77640df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:a5f845c4a1d81ca6aab7635ed73ca31a6a1c726466b78927b7aa1b766b3b2d74
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219527256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293ef5aca12c193a7ca04e27ef23bfa659360ac667b0e24aa1fa7edd1c2ccce2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 19:39:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 26 Nov 2020 18:21:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 26 Nov 2020 18:21:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 26 Nov 2020 18:21:19 GMT
ENV PS_VERSION=5.7.32-35.1
# Thu, 26 Nov 2020 18:21:19 GMT
ENV OS_VER=el8
# Thu, 26 Nov 2020 18:21:19 GMT
ENV FULL_PERCONA_VERSION=5.7.32-35.1.el8
# Thu, 26 Nov 2020 18:21:58 GMT
RUN set -ex;     dnf install -y         dnf-utils         jemalloc         cracklib-dicts         which;         repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         selinux-policy             | xargs curl -Lf -o /tmp/selinux-policy.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/selinux-policy.rpm --nodeps;     rm -rf /tmp/policycoreutils.rpm /tmp/selinux-policy.rpm;         dnf install -y         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf remove -y dnf-utils;     dnf clean all;     rm -rf /var/cache/dnf /var/lib/mysql
# Thu, 26 Nov 2020 18:21:59 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 26 Nov 2020 18:22:00 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 26 Nov 2020 18:22:00 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Thu, 26 Nov 2020 18:22:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Nov 2020 18:22:00 GMT
USER mysql
# Thu, 26 Nov 2020 18:22:00 GMT
EXPOSE 3306
# Thu, 26 Nov 2020 18:22:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5161ecf9ba2fca57c589f8f9792e900e91275c33e936dd451f9a2997e7b603e`  
		Last Modified: Thu, 26 Nov 2020 18:23:23 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a9d3ae780cab7fb8604cf11602aabbd7b99ade4ea988076f6990998d9be82`  
		Last Modified: Thu, 26 Nov 2020 18:23:25 GMT  
		Size: 29.6 MB (29572775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d858105f627575ba36e73af8f7d480a34e362199b91e66a6a1d1717c00f257`  
		Last Modified: Thu, 26 Nov 2020 18:23:42 GMT  
		Size: 115.1 MB (115080362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210772ab6e7769306588cdc50a49b5f3ccf6a75f2c2e366827e27254ee9b02f7`  
		Last Modified: Thu, 26 Nov 2020 18:23:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b688371fc037c34d9bc8d31b3e6ea456e27117eaa7bf1ae2fb27f0f9e29b692`  
		Last Modified: Thu, 26 Nov 2020 18:23:24 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
