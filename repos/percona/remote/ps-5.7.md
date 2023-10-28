## `percona:ps-5.7`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:d490c6e853cd2e2cc776abde844802b9d4ac18909d93de8d1d1e4ca633a96157
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.7 MB (426726358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56732f613ee9b9b6a8b964274165de430479db4d4b4f76303e3336ba09d1bb61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:48:18 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 28 Oct 2023 03:48:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 28 Oct 2023 03:48:55 GMT
ENV PS_VERSION=5.7.43-47.1
# Sat, 28 Oct 2023 03:48:55 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:48:55 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Sat, 28 Oct 2023 03:49:32 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 28 Oct 2023 03:49:34 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 28 Oct 2023 03:49:34 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 28 Oct 2023 03:49:34 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 28 Oct 2023 03:49:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 03:49:34 GMT
USER mysql
# Sat, 28 Oct 2023 03:49:34 GMT
EXPOSE 3306
# Sat, 28 Oct 2023 03:49:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e708b4947f6e5cc913e5fc045d0257220c0af7ae1021abca04fc21e24a7b83`  
		Last Modified: Sat, 28 Oct 2023 03:54:50 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af84e34f2de90f5f24b163becff558f8932de39150f5536253f55303a685309e`  
		Last Modified: Sat, 28 Oct 2023 03:55:01 GMT  
		Size: 201.1 MB (201051082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1130027dc6062a2db6fbb519792dcf95a96285ec0e33fc516eb04ffdacbcf8c0`  
		Last Modified: Sat, 28 Oct 2023 03:55:07 GMT  
		Size: 137.7 MB (137664751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10dc21892e9bbf749cf4cf54b41056cb1b7cfaa726c0d37ff076743bd94b57`  
		Last Modified: Sat, 28 Oct 2023 03:54:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9457052f5b00446c1a1ccb3793be2f34dcbd45dc997da7ca00d9513cb393136c`  
		Last Modified: Sat, 28 Oct 2023 03:54:50 GMT  
		Size: 3.1 KB (3063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
