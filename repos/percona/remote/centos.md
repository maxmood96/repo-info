## `percona:centos`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:031a74beb5844614beadaaed576b4b144de64463f4d4f9079d807299a6568968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.1 MB (426067079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb12560d2c4aa51e14bd9fa07e68de9079fd6c4bbd3a09974045a302d311145`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:48:25 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:49:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 20 Oct 2023 18:49:01 GMT
ENV PS_VERSION=5.7.43-47.1
# Fri, 20 Oct 2023 18:49:01 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:49:01 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Fri, 20 Oct 2023 18:49:41 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:49:42 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 20 Oct 2023 18:49:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:49:42 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:49:43 GMT
USER mysql
# Fri, 20 Oct 2023 18:49:43 GMT
EXPOSE 3306
# Fri, 20 Oct 2023 18:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf0ca6bec673809c43d44713e2a647bf67fbdaa9ed4f8fd7c46f835388c21e9`  
		Last Modified: Fri, 20 Oct 2023 18:56:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ecfbe81e489c18be2cb987a7f218c48a2dc00fd91c0260a33abd5d72c3a5cf`  
		Last Modified: Fri, 20 Oct 2023 18:56:22 GMT  
		Size: 200.4 MB (200400348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e90e85f06888382f27e6f90f7dc0903a8c5272a565c60df6b77a6920ba5c8b4`  
		Last Modified: Fri, 20 Oct 2023 18:56:28 GMT  
		Size: 137.7 MB (137657560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a3e0a101f98ccea4da1d570b6eb81d4fb12876069064b8264ec50e4b1a2a59`  
		Last Modified: Fri, 20 Oct 2023 18:56:10 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd3c7a4001aa5863a2d6c72f80b1925f924038bcecefb7a2b5a787771452dcf`  
		Last Modified: Fri, 20 Oct 2023 18:56:10 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
