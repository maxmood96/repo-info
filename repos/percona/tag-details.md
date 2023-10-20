<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:5`](#percona5)
-	[`percona:5-centos`](#percona5-centos)
-	[`percona:5.6`](#percona56)
-	[`percona:5.6-centos`](#percona56-centos)
-	[`percona:5.6.51-2`](#percona5651-2)
-	[`percona:5.6.51-2-centos`](#percona5651-2-centos)
-	[`percona:5.7`](#percona57)
-	[`percona:5.7-centos`](#percona57-centos)
-	[`percona:5.7.43`](#percona5743)
-	[`percona:5.7.43-centos`](#percona5743-centos)
-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.34-26`](#percona8034-26)
-	[`percona:8.0.34-26-centos`](#percona8034-26-centos)
-	[`percona:centos`](#perconacentos)
-	[`percona:ps-5`](#perconaps-5)
-	[`percona:ps-5.6`](#perconaps-56)
-	[`percona:ps-5.6.51-2`](#perconaps-5651-2)
-	[`percona:ps-5.7`](#perconaps-57)
-	[`percona:ps-5.7.43`](#perconaps-5743)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.34-26`](#perconaps-8034-26)
-	[`percona:psmdb-4.2`](#perconapsmdb-42)
-	[`percona:psmdb-4.2.24`](#perconapsmdb-4224)
-	[`percona:psmdb-4.4`](#perconapsmdb-44)
-	[`percona:psmdb-4.4.22`](#perconapsmdb-4422)
-	[`percona:psmdb-5.0`](#perconapsmdb-50)
-	[`percona:psmdb-5.0.18`](#perconapsmdb-5018)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.6`](#perconapsmdb-606)

## `percona:5`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

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

## `percona:5-centos`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

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

## `percona:5.6`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.6` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6-centos`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.6-centos` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6.51-2`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.6.51-2` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6.51-2-centos`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.6.51-2-centos` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

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

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

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

## `percona:5.7.43`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43` - linux; amd64

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

## `percona:5.7.43-centos`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43-centos` - linux; amd64

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

## `percona:8`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26-centos`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26-centos` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `percona:ps-5`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

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

## `percona:ps-5.6`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.6` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.6.51-2`

```console
$ docker pull percona@sha256:8c915f6fff3a43383938b4015ee3740dc1886fd5016a1404ff45b55de71e49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.6.51-2` - linux; amd64

```console
$ docker pull percona@sha256:a865615cf007e34fc520a72786a807909f8c75fd233388a0a0445fa82b5319cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195312192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1d76c933806bd31b1a5833d091c41c5bc6c9d0953c4a2c764668d37c6f79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:58:17 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 18:58:18 GMT
RUN groupdel input && groupadd -g 999 mysql
# Wed, 15 Sep 2021 18:58:19 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Dec 2021 19:25:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;         curl -Lf -o /tmp/nss.rpm http://mirror.centos.org/centos/7/updates/x86_64/Packages/nss-3.67.0-4.el7_9.x86_64.rpm;     rpmkeys --checksig /tmp/nss.rpm;     yum install -y /tmp/nss.rpm;         rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;         percona-release disable all;     percona-release enable original release
# Thu, 30 Dec 2021 19:25:25 GMT
ENV PERCONA_VERSION=5.6.51-rel91.0.1.el7
# Thu, 30 Dec 2021 19:36:53 GMT
RUN set -ex;     yum install -y         Percona-Server-server-56-${PERCONA_VERSION}         Percona-Server-tokudb-56-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 30 Dec 2021 19:36:55 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 30 Dec 2021 19:36:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 30 Dec 2021 19:36:55 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Thu, 30 Dec 2021 19:36:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Dec 2021 19:36:56 GMT
USER mysql
# Thu, 30 Dec 2021 19:36:56 GMT
EXPOSE 3306
# Thu, 30 Dec 2021 19:36:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd68507e31292f16aa2d29907b401abd6ab53be7b485f2bdea2a7182e63d1af`  
		Last Modified: Wed, 15 Sep 2021 19:05:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee280aea028899106d471852f72f47591667f5edf38214be74a6121932ea56`  
		Last Modified: Wed, 15 Sep 2021 19:05:49 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729721338aa7f33aa759726ffa7b1c50288e2dcae602d0323eecab0ff98c9c26`  
		Last Modified: Thu, 30 Dec 2021 19:38:06 GMT  
		Size: 59.7 MB (59728568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8b9873953ce124f23ca0f1406a9518ca744b77cfbebdd6d9f79a785fa7a09`  
		Last Modified: Thu, 30 Dec 2021 19:38:08 GMT  
		Size: 59.5 MB (59476470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c076538b02993035990718d78a0b06fe3a6fc95b571ce334ae270c2cd4cc8`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1806011b64a9860267de7f898bd25bd33c0a6a69901dc7f8319e855bea3c1303`  
		Last Modified: Thu, 30 Dec 2021 19:37:58 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

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

## `percona:ps-5.7.43`

```console
$ docker pull percona@sha256:559dea56d1ca9f5cfae0582c9bc22081306d73e81b5805cbf3a0baee69f848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.43` - linux; amd64

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

## `percona:ps-8`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.34-26`

```console
$ docker pull percona@sha256:8bdc8687dcebb01695f11d23a0f288cc6099184d434a434ff1392268d4f5741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:3368b4007a91dccc45dde476726dc194ea710ac7ebcd5ff18e3b3e6e6947d060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387532992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfca9b80e314601d6ffe18fa9ea1de3749bcf2e8ea36cd6e6ec7fc95e4e06d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:26:45 GMT
ADD file:65ff87b4fa664532e0d517be6317319b917d272116beb71cbf937449303720c1 in / 
# Fri, 20 Oct 2023 18:26:46 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:47:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:47:15 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 20 Oct 2023 18:47:16 GMT
ENV OS_VER=el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 20 Oct 2023 18:47:16 GMT
ENV PS_REPO=release
# Fri, 20 Oct 2023 18:47:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 20 Oct 2023 18:48:16 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 20 Oct 2023 18:48:20 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 20 Oct 2023 18:48:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 20 Oct 2023 18:48:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 20 Oct 2023 18:48:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Oct 2023 18:48:21 GMT
USER mysql
# Fri, 20 Oct 2023 18:48:21 GMT
EXPOSE 3306 33060
# Fri, 20 Oct 2023 18:48:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a88aa7d144c2ee2eadb5e6717bdc20b913a602d3ac114461729f62d4ca50ad02`  
		Last Modified: Fri, 20 Oct 2023 18:28:11 GMT  
		Size: 88.0 MB (87988385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a57b1efaa84397844bab9a395f1d3e60b03ce0aa0052deab3cba6d141f888c2`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8ce3c76b4fbb80f48f42c554e79c96d29af235b68177912f1e125ef07a92c4`  
		Last Modified: Fri, 20 Oct 2023 18:55:07 GMT  
		Size: 7.3 MB (7314442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693782b8ff0c664f612261ece1e7351d6fff926303254c95ff0ce92c2152c42b`  
		Last Modified: Fri, 20 Oct 2023 18:55:45 GMT  
		Size: 292.2 MB (292224277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4f50d2cd384025badedbf8c451c6c0231fa44b67961262e59035afad257f4`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefab14aeb92409fcf7c683dffbbd5166db44f165c6ce2b21b30029ee2019be`  
		Last Modified: Fri, 20 Oct 2023 18:55:05 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:799d42e7a21d7f9d3b9fdec8d2b6a572e4dacc99d91acc79a03e58bcd2e3dd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:1eb76f7a23a1fa913a225b92478f465b943c2418e313b9dc25b62b15f6c01617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218145742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79b2bdcfa189f9b5d7a7312c8307a6d416cb643e918175d39389d5181bd6d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 20 Oct 2023 18:53:35 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:53:38 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:54:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:54:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:54:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:54:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:54:28 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:54:31 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:54:33 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:54:33 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:54:34 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:54:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:54:34 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:54:34 GMT
USER 1001
# Fri, 20 Oct 2023 18:54:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76795c0899241325dcb841525263bfd026e68ae397792bc5bbfc9d24f844036`  
		Last Modified: Fri, 20 Oct 2023 18:58:34 GMT  
		Size: 3.8 MB (3797333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1636e9f4b2007a174616e0afcaa4483df12d019137b556fd6f597508ed89c1`  
		Last Modified: Fri, 20 Oct 2023 18:58:48 GMT  
		Size: 117.3 MB (117257972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd71f3c4c238975cf62751c23db53c57a6305c654d6d8fa92ea85103dc69a2`  
		Last Modified: Fri, 20 Oct 2023 18:58:33 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b324880d43da00be84772170373031e04f83e8968d30558c39b43a00686f5504`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a45ce4781f928b7d7a708774c9a1413a06ef2d4834cfe160173c28e89fcbb2`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158a8bd7b1882440261d387042b11f1edb14d3822490dab2df05d66d732017e`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f665c9c567a036881bb25a0750636f87264ca52434e43d8cca0f0ff228081f`  
		Last Modified: Fri, 20 Oct 2023 18:58:32 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958128413188fd5a6a1d46e2692b1ad8d0e18328aa08d35c69dca8ec24bdfe9`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:799d42e7a21d7f9d3b9fdec8d2b6a572e4dacc99d91acc79a03e58bcd2e3dd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:1eb76f7a23a1fa913a225b92478f465b943c2418e313b9dc25b62b15f6c01617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218145742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79b2bdcfa189f9b5d7a7312c8307a6d416cb643e918175d39389d5181bd6d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 20 Oct 2023 18:53:35 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:53:38 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:54:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:54:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:54:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:54:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:54:28 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:54:31 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:54:33 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:54:33 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:54:34 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:54:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:54:34 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:54:34 GMT
USER 1001
# Fri, 20 Oct 2023 18:54:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76795c0899241325dcb841525263bfd026e68ae397792bc5bbfc9d24f844036`  
		Last Modified: Fri, 20 Oct 2023 18:58:34 GMT  
		Size: 3.8 MB (3797333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1636e9f4b2007a174616e0afcaa4483df12d019137b556fd6f597508ed89c1`  
		Last Modified: Fri, 20 Oct 2023 18:58:48 GMT  
		Size: 117.3 MB (117257972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd71f3c4c238975cf62751c23db53c57a6305c654d6d8fa92ea85103dc69a2`  
		Last Modified: Fri, 20 Oct 2023 18:58:33 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b324880d43da00be84772170373031e04f83e8968d30558c39b43a00686f5504`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a45ce4781f928b7d7a708774c9a1413a06ef2d4834cfe160173c28e89fcbb2`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158a8bd7b1882440261d387042b11f1edb14d3822490dab2df05d66d732017e`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f665c9c567a036881bb25a0750636f87264ca52434e43d8cca0f0ff228081f`  
		Last Modified: Fri, 20 Oct 2023 18:58:32 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958128413188fd5a6a1d46e2692b1ad8d0e18328aa08d35c69dca8ec24bdfe9`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:0b305b658c51894969bf1f04a1cde45e44ee82442b90daf7a24e2be0923beb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:66a119fbf4b736c04065e03718bd011cdfb3190df9ade5ab68dd08b9a92041e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236689421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1be01405927244423480268f86573a25928235a6793e3c5baa0550fd5900839`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:52:25 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 20 Oct 2023 18:52:25 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:52:25 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 20 Oct 2023 18:52:25 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:52:25 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:53:17 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:53:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:53:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:53:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:53:19 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:53:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:53:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:53:24 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:53:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:53:25 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 20 Oct 2023 18:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:53:25 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:53:25 GMT
USER 1001
# Fri, 20 Oct 2023 18:53:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efa3f47dafc3227c24f96744d0a76618e9e4334074e53053fdcec6a90f8753`  
		Last Modified: Fri, 20 Oct 2023 18:58:20 GMT  
		Size: 135.8 MB (135802048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d5a6b42d98bca611002a4ea27586ad542f9ff58e2d6ae57d02d0ef0d11f99`  
		Last Modified: Fri, 20 Oct 2023 18:58:03 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72937c4fd736908341cb3c4dc4c3bf4eaca54edfc77bc2d15ee9dbec9f92cbe5`  
		Last Modified: Fri, 20 Oct 2023 18:58:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7f2753fd5c751daca23604e08ef9dd05731bdf67d8a5e3c684a6d044acb26`  
		Last Modified: Fri, 20 Oct 2023 18:58:01 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468cfa3e9cc261d76f6988c33d9579c9b8a71652f8e24f84199a19f6efb1ead9`  
		Last Modified: Fri, 20 Oct 2023 18:58:02 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09172bf6e1653c3b7d8908ab6aec0c195544a58b1f6c3dcd6378fb91434db8`  
		Last Modified: Fri, 20 Oct 2023 18:58:03 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f8b1b52d5dc409a03a92f45772c7404baef33f22625197b8a100ea919f23ba`  
		Last Modified: Fri, 20 Oct 2023 18:58:01 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337b4438df66518c04e15a6d6c7517f53291bc839996facf35e2fdb1b5d88495`  
		Last Modified: Fri, 20 Oct 2023 18:58:02 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:0b305b658c51894969bf1f04a1cde45e44ee82442b90daf7a24e2be0923beb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:66a119fbf4b736c04065e03718bd011cdfb3190df9ade5ab68dd08b9a92041e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236689421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1be01405927244423480268f86573a25928235a6793e3c5baa0550fd5900839`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:52:25 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 20 Oct 2023 18:52:25 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:52:25 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 20 Oct 2023 18:52:25 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:52:25 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:53:17 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:53:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:53:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:53:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:53:19 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:53:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:53:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:53:24 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:53:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:53:25 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 20 Oct 2023 18:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:53:25 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:53:25 GMT
USER 1001
# Fri, 20 Oct 2023 18:53:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efa3f47dafc3227c24f96744d0a76618e9e4334074e53053fdcec6a90f8753`  
		Last Modified: Fri, 20 Oct 2023 18:58:20 GMT  
		Size: 135.8 MB (135802048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d5a6b42d98bca611002a4ea27586ad542f9ff58e2d6ae57d02d0ef0d11f99`  
		Last Modified: Fri, 20 Oct 2023 18:58:03 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72937c4fd736908341cb3c4dc4c3bf4eaca54edfc77bc2d15ee9dbec9f92cbe5`  
		Last Modified: Fri, 20 Oct 2023 18:58:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7f2753fd5c751daca23604e08ef9dd05731bdf67d8a5e3c684a6d044acb26`  
		Last Modified: Fri, 20 Oct 2023 18:58:01 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468cfa3e9cc261d76f6988c33d9579c9b8a71652f8e24f84199a19f6efb1ead9`  
		Last Modified: Fri, 20 Oct 2023 18:58:02 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad09172bf6e1653c3b7d8908ab6aec0c195544a58b1f6c3dcd6378fb91434db8`  
		Last Modified: Fri, 20 Oct 2023 18:58:03 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f8b1b52d5dc409a03a92f45772c7404baef33f22625197b8a100ea919f23ba`  
		Last Modified: Fri, 20 Oct 2023 18:58:01 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337b4438df66518c04e15a6d6c7517f53291bc839996facf35e2fdb1b5d88495`  
		Last Modified: Fri, 20 Oct 2023 18:58:02 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:c4c9ec2e4d3afad1979cd2f1456ba3cb3391f709a342945e056289acba7bbd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:5cef7dfd8e38103ce134545850f1d69e77c47c8da95edda57525de5b26515e0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249303274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de03226b2b13f63764d376aedf876266afec4dd545967e9173d3ca7f8c9b156`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 20 Oct 2023 18:51:15 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:52:07 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:52:08 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:52:08 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:52:08 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:52:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:52:11 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:52:13 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:52:13 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:52:14 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:52:14 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:52:14 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:52:14 GMT
USER 1001
# Fri, 20 Oct 2023 18:52:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6c785ca3a6fc517f1ba95a76c07abafa8684d465949dd4a1ababdaccae046`  
		Last Modified: Fri, 20 Oct 2023 18:57:51 GMT  
		Size: 148.4 MB (148415890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ed5695fb2672d04a5850c0aea73ea95914a13ff36b7e9a9bedcf8670bd6e1`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ed65b64b1416138d3570a58560feb319a70fc6eb47e75a7b3db6a3cd8e4165`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214e38aea4a7fcf729fe79b1ae1c8b8a4099cf172dc4ae781f7ef0c9236267f4`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be724c7b226f4fd713f609122402617f49aa061abe71ec550bcfa7f003bf2c`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbad2e3b812c4ef4531a43fb396a68b3033af65beb7c207424e2c8b18326dd06`  
		Last Modified: Fri, 20 Oct 2023 18:57:33 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66459148337569d2008b5bc277f313d2f2f27199f74b0b2ef0c4eb7d4150415`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b049ff67cf7d690c2893e1f4a928baa052006e8f3bb55f990d9b994767fd5`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:c4c9ec2e4d3afad1979cd2f1456ba3cb3391f709a342945e056289acba7bbd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:5cef7dfd8e38103ce134545850f1d69e77c47c8da95edda57525de5b26515e0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249303274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de03226b2b13f63764d376aedf876266afec4dd545967e9173d3ca7f8c9b156`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 20 Oct 2023 18:51:15 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:52:07 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:52:08 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:52:08 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:52:08 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:52:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:52:11 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:52:13 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:52:13 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:52:14 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:52:14 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:52:14 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:52:14 GMT
USER 1001
# Fri, 20 Oct 2023 18:52:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6c785ca3a6fc517f1ba95a76c07abafa8684d465949dd4a1ababdaccae046`  
		Last Modified: Fri, 20 Oct 2023 18:57:51 GMT  
		Size: 148.4 MB (148415890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ed5695fb2672d04a5850c0aea73ea95914a13ff36b7e9a9bedcf8670bd6e1`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ed65b64b1416138d3570a58560feb319a70fc6eb47e75a7b3db6a3cd8e4165`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214e38aea4a7fcf729fe79b1ae1c8b8a4099cf172dc4ae781f7ef0c9236267f4`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be724c7b226f4fd713f609122402617f49aa061abe71ec550bcfa7f003bf2c`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbad2e3b812c4ef4531a43fb396a68b3033af65beb7c207424e2c8b18326dd06`  
		Last Modified: Fri, 20 Oct 2023 18:57:33 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66459148337569d2008b5bc277f313d2f2f27199f74b0b2ef0c4eb7d4150415`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b049ff67cf7d690c2893e1f4a928baa052006e8f3bb55f990d9b994767fd5`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:2c17da21041eaa6db6502ca09d20c0bf1a5b883eb7beee7bb32feace2eb025a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:3d33e689e759b14ac0a5311ecfa3aa1199804ca9b2ff2a0a57da129aee3a1c39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272720869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9abd907c76d0580cda6ba351756bf900981024ade2577fca92820ad463456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 20 Oct 2023 18:49:54 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:50:52 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:50:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:50:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:50:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:50:54 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:50:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:51:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:51:01 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:51:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:51:02 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:51:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:51:02 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:51:02 GMT
USER 1001
# Fri, 20 Oct 2023 18:51:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee6cf1d770291d43a5eb143e2f090d5af63cad0af98e166a7f85bd8334bad19`  
		Last Modified: Fri, 20 Oct 2023 18:57:21 GMT  
		Size: 171.8 MB (171833487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b944b5db72b60ab4ab1bc3b795d4ff540f36ebf182c9a09bbb080efd4e6964`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c844be69bbd9131d529da8130e5432a09df5dd8eedbec2f667caf5fb823ccf95`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678645bfac4c586b67c5daa11858d85aa2c45d261e26f9242e6c83a12b66844`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c15daa0f6d6c8f88f6ab0f79f2f0628a0041c1fe4d2d3de162df628301f828e`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8fbec1e977f341c4b291cfab3a1aaef7364afd23bf5dd9bfad01fa80751a7`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529923280384227121299eabe5064c06d1ba7087bf293fe486758a445e8fe2c`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f58b0257aff2f7f4ba0a404508938f088851f06b5fe8eed4e8300b0bbe7f58`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:2c17da21041eaa6db6502ca09d20c0bf1a5b883eb7beee7bb32feace2eb025a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:3d33e689e759b14ac0a5311ecfa3aa1199804ca9b2ff2a0a57da129aee3a1c39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272720869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9abd907c76d0580cda6ba351756bf900981024ade2577fca92820ad463456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 20 Oct 2023 18:49:54 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:50:52 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:50:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:50:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:50:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:50:54 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:50:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:51:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:51:01 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:51:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:51:02 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:51:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:51:02 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:51:02 GMT
USER 1001
# Fri, 20 Oct 2023 18:51:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee6cf1d770291d43a5eb143e2f090d5af63cad0af98e166a7f85bd8334bad19`  
		Last Modified: Fri, 20 Oct 2023 18:57:21 GMT  
		Size: 171.8 MB (171833487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b944b5db72b60ab4ab1bc3b795d4ff540f36ebf182c9a09bbb080efd4e6964`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c844be69bbd9131d529da8130e5432a09df5dd8eedbec2f667caf5fb823ccf95`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678645bfac4c586b67c5daa11858d85aa2c45d261e26f9242e6c83a12b66844`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c15daa0f6d6c8f88f6ab0f79f2f0628a0041c1fe4d2d3de162df628301f828e`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8fbec1e977f341c4b291cfab3a1aaef7364afd23bf5dd9bfad01fa80751a7`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529923280384227121299eabe5064c06d1ba7087bf293fe486758a445e8fe2c`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f58b0257aff2f7f4ba0a404508938f088851f06b5fe8eed4e8300b0bbe7f58`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
