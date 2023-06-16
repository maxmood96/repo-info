## `percona:ps-8`

```console
$ docker pull percona@sha256:f023a737c701d4b87f9980cc8346df0b3eb4f08e57bf3c7a90d20f656fb5584e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:4b0ec491ba8637e2888f0a0e3adfad51a868f035c7c263c368f9e71adb5df65d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344594027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5071f705a75758669d0400445e7aeb3f230260abed7717028f089009b090e8f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jun 2023 00:20:10 GMT
ADD file:4d6795a06ab65ed16d9773d6062cfb26d1cc84e8d1d57a4ab57acc3ad355bc28 in / 
# Fri, 16 Jun 2023 00:20:11 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:44:39 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 16 Jun 2023 00:44:40 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 16 Jun 2023 00:44:40 GMT
ENV PS_VERSION=8.0.32-24.1
# Fri, 16 Jun 2023 00:44:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1
# Fri, 16 Jun 2023 00:44:40 GMT
ENV OS_VER=el9
# Fri, 16 Jun 2023 00:44:40 GMT
ENV FULL_PERCONA_VERSION=8.0.32-24.1.el9
# Fri, 16 Jun 2023 00:44:40 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.32-1.el9
# Fri, 16 Jun 2023 00:44:40 GMT
ENV PS_REPO=testing
# Fri, 16 Jun 2023 00:44:43 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 16 Jun 2023 00:45:27 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 16 Jun 2023 00:45:30 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 16 Jun 2023 00:45:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 16 Jun 2023 00:45:30 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 16 Jun 2023 00:45:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 00:45:30 GMT
USER mysql
# Fri, 16 Jun 2023 00:45:30 GMT
EXPOSE 3306 33060
# Fri, 16 Jun 2023 00:45:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd3a74881334e44c59cd7aa126040b4e8f5429f27370e87c3bf0857becd84786`  
		Last Modified: Fri, 16 Jun 2023 00:21:29 GMT  
		Size: 88.0 MB (87963873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe174e5edf9341715af80f2f73266079ce90b84b1293a6e2878004eca2dae3e`  
		Last Modified: Fri, 16 Jun 2023 00:49:01 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a307017dd78b2e32f076ec33dbf46c74cf0caa1376438a56f1e72d7f3177e8`  
		Last Modified: Fri, 16 Jun 2023 00:49:02 GMT  
		Size: 7.3 MB (7330246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c02a840c5c7f1c5439acf44455e6fed9774726aa6f2f864a94475a2e53ac5`  
		Last Modified: Fri, 16 Jun 2023 00:49:33 GMT  
		Size: 249.3 MB (249294021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6c497a7dc57af7ef6626d638a5d2c3c93b955d470be03717383e46bb23f94`  
		Last Modified: Fri, 16 Jun 2023 00:49:01 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489634d71ccf3405d7b8020c3a9d360a4edcaca8f8f7f83a2b8eb008b5ce5adf`  
		Last Modified: Fri, 16 Jun 2023 00:49:01 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
