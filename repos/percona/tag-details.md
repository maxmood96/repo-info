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
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

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

## `percona:5-centos`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

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
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

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

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

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

## `percona:5.7.43`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43` - linux; amd64

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

## `percona:5.7.43-centos`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43-centos` - linux; amd64

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

## `percona:8`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26-centos`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26-centos` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

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

## `percona:ps-5`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

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

## `percona:ps-5.7.43`

```console
$ docker pull percona@sha256:d249642625bc28a836cae58ec9bb8999687a78c7aa6f11187393847b00bc319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.43` - linux; amd64

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

## `percona:ps-8`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.34-26`

```console
$ docker pull percona@sha256:5986a5788d384bd8af0694d2821e43d01945e0a72f119e5fe9784079e4fa0c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:3bf65e9ef693fe798cff664695b0ce4b9b8ba505465394bf7df7a29342334ee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393840912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c442664bf9d067b9b4d4e1ab489308d3cf758ff942e76f6418fe1d61bf1315d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Nov 2023 20:30:37 GMT
ADD file:cae1767b6ea3d1e31d5b768d10050817d64306ad02266a0a88b7122709dde7d5 in / 
# Thu, 16 Nov 2023 20:30:37 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 21:02:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 16 Nov 2023 21:02:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 16 Nov 2023 21:02:04 GMT
ENV OS_VER=el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 16 Nov 2023 21:02:04 GMT
ENV PS_REPO=release
# Thu, 16 Nov 2023 21:02:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 16 Nov 2023 21:03:08 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 16 Nov 2023 21:03:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 16 Nov 2023 21:03:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 16 Nov 2023 21:03:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 16 Nov 2023 21:03:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Nov 2023 21:03:13 GMT
USER mysql
# Thu, 16 Nov 2023 21:03:13 GMT
EXPOSE 3306 33060
# Thu, 16 Nov 2023 21:03:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3205519495f29f0b21d5a3f9c9444fa01cd2d7096a769633b2f0ccc0df17eead`  
		Last Modified: Thu, 16 Nov 2023 20:31:45 GMT  
		Size: 94.3 MB (94347722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0783f734401244d3e73aa40db52ccc3b61833533f4ecab45624de6090562b`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a603ba7564742994d569fd3772fdfd3caf729284dac9c6bca45d4396dcd8f0e`  
		Last Modified: Thu, 16 Nov 2023 21:03:59 GMT  
		Size: 7.3 MB (7294857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fbdf378966af0264a9f6a2d2d4a209a69dba4e3ef4fd182d6c438b82571ef4`  
		Last Modified: Thu, 16 Nov 2023 21:04:38 GMT  
		Size: 292.2 MB (292192455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4cf865b2e68b3a1e70a20d2fce723fb33be1f086d476c015fdd8d7ea437d91`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c5716bc433d6a10f0a50a30ed713a095fd3f018441d68ef71b5c8809925fe0`  
		Last Modified: Thu, 16 Nov 2023 21:03:58 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:74761747d355301a1d38fa59a0c29c31087a0973725114bc05fb6cd4aef4c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:740a210c719ab774d451ff24d1fec8836a54b83f7e2c7c617a04f706b0058f96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218126011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723d220fe3f8870c53d88843c03d7b858917fc6e3861af6added68494279a0cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 28 Oct 2023 03:53:14 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:53:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:54:04 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:54:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:54:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:54:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:54:06 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:54:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:54:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:54:11 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:54:11 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:54:11 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:54:11 GMT
USER 1001
# Sat, 28 Oct 2023 03:54:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea63e2471396fb3eafc4042ce991f96da511443b418212d7ad8c326199d2cf`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 3.8 MB (3787465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51032f70d0821cf41c15684232cf756663ba7288db50655496bd03b85acc342e`  
		Last Modified: Sat, 28 Oct 2023 03:57:20 GMT  
		Size: 117.2 MB (117246763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b405104fc2a9b3b3fa936bba18ef021014e9348dd8c70c66e9fb6762513baca`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d8db8dc48968264c1516d3ec031d58aa1b262d27a4e1e16cf15a59305e143`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a48b2ee810ca3fbbf924e3928b3a687e6db5fb25126c3af1b8a17a5343b410`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed26e5f822fc5e75c7b5dccfb2771db943f353d591fd54227450376f9c181abb`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2839ab117c76045e458ccfcc12efa69ead2c9bc8836d58de960187104c85181`  
		Last Modified: Sat, 28 Oct 2023 03:57:05 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0810186cf8a50eebd3483cb237f80250d90c3be190db708b94136cc2bff06c60`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:74761747d355301a1d38fa59a0c29c31087a0973725114bc05fb6cd4aef4c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:740a210c719ab774d451ff24d1fec8836a54b83f7e2c7c617a04f706b0058f96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218126011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723d220fe3f8870c53d88843c03d7b858917fc6e3861af6added68494279a0cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 28 Oct 2023 03:53:14 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:53:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:54:04 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:54:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:54:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:54:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:54:06 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:54:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:54:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:54:11 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:54:11 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:54:11 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:54:11 GMT
USER 1001
# Sat, 28 Oct 2023 03:54:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea63e2471396fb3eafc4042ce991f96da511443b418212d7ad8c326199d2cf`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 3.8 MB (3787465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51032f70d0821cf41c15684232cf756663ba7288db50655496bd03b85acc342e`  
		Last Modified: Sat, 28 Oct 2023 03:57:20 GMT  
		Size: 117.2 MB (117246763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b405104fc2a9b3b3fa936bba18ef021014e9348dd8c70c66e9fb6762513baca`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d8db8dc48968264c1516d3ec031d58aa1b262d27a4e1e16cf15a59305e143`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a48b2ee810ca3fbbf924e3928b3a687e6db5fb25126c3af1b8a17a5343b410`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed26e5f822fc5e75c7b5dccfb2771db943f353d591fd54227450376f9c181abb`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2839ab117c76045e458ccfcc12efa69ead2c9bc8836d58de960187104c85181`  
		Last Modified: Sat, 28 Oct 2023 03:57:05 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0810186cf8a50eebd3483cb237f80250d90c3be190db708b94136cc2bff06c60`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:4e71e7839bda28a725251414f385e8d6391bb4d41a706d4bd7a601b7b7faf52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:7c52eee26ff412ecb3969702bebfc5d69b30d662ec4e05f0a2a026ca61ca3f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236661972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a979a1c9b8b0942e8274d850ed68b05cfaef5c36f19f765ce088c3882985391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 28 Oct 2023 03:52:04 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:52:53 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:52:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:52:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:52:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:52:55 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:52:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:52:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:52:59 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:53:00 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:53:00 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 28 Oct 2023 03:53:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:53:00 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:53:00 GMT
USER 1001
# Sat, 28 Oct 2023 03:53:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901eb5560838581fe3fce62b3efdef0fee4308c62952ab1fa784ccf850d4fbe1`  
		Last Modified: Sat, 28 Oct 2023 03:56:54 GMT  
		Size: 135.8 MB (135783073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e93c997c7436b089aee1ff21a7046993db82e76be1f473bca8ef1081e20bb87`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc2ddf356b06d5c0ced8bc092ed85ec13ee2a80b22dc0902567b93a144814d`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca40975bfce537fd3ba2afaafa8b7f4466f7b0618397e64e81002c4722bec0`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626c15e195538af552f994c1480521353f448dc299a37bc02898b6ff293092bc`  
		Last Modified: Sat, 28 Oct 2023 03:56:36 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ff487a177f0b835f47e8e9b11e215551a3b343b9efeba653a0207b0020d0b`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a554d2942b045fa604731729991c6082011f49fe29bb73a6b9f8a36fbf3cf8`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77309a77b170f62ef51c0cb3f30115c328c88ae314117ef4b63f5b8d3cdd7d5a`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:4e71e7839bda28a725251414f385e8d6391bb4d41a706d4bd7a601b7b7faf52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:7c52eee26ff412ecb3969702bebfc5d69b30d662ec4e05f0a2a026ca61ca3f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236661972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a979a1c9b8b0942e8274d850ed68b05cfaef5c36f19f765ce088c3882985391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 28 Oct 2023 03:52:04 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:52:53 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:52:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:52:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:52:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:52:55 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:52:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:52:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:52:59 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:53:00 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:53:00 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 28 Oct 2023 03:53:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:53:00 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:53:00 GMT
USER 1001
# Sat, 28 Oct 2023 03:53:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901eb5560838581fe3fce62b3efdef0fee4308c62952ab1fa784ccf850d4fbe1`  
		Last Modified: Sat, 28 Oct 2023 03:56:54 GMT  
		Size: 135.8 MB (135783073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e93c997c7436b089aee1ff21a7046993db82e76be1f473bca8ef1081e20bb87`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc2ddf356b06d5c0ced8bc092ed85ec13ee2a80b22dc0902567b93a144814d`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca40975bfce537fd3ba2afaafa8b7f4466f7b0618397e64e81002c4722bec0`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626c15e195538af552f994c1480521353f448dc299a37bc02898b6ff293092bc`  
		Last Modified: Sat, 28 Oct 2023 03:56:36 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ff487a177f0b835f47e8e9b11e215551a3b343b9efeba653a0207b0020d0b`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a554d2942b045fa604731729991c6082011f49fe29bb73a6b9f8a36fbf3cf8`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77309a77b170f62ef51c0cb3f30115c328c88ae314117ef4b63f5b8d3cdd7d5a`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:efc61ce60a9d514a1b062a2b8615309294f71b273b4b7f5b3ce33ef273a36c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:b4c00f3d522ecf35085669952a1e7f8d3bc653c6db8d2ea06745067b7451608b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249278501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7774313fed89667efbcb292dcce4d79ad5a6e1e9fed4140ab8d8047e00642274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 28 Oct 2023 03:50:54 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:51:44 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:51:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:51:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:51:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:51:46 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:51:49 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:51:51 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:51:51 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:51:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:51:52 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:51:52 GMT
USER 1001
# Sat, 28 Oct 2023 03:51:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a605fb25d797064c47be29eb769c24e001d08f5e8d62528c9efe7f6975e29c27`  
		Last Modified: Sat, 28 Oct 2023 03:56:27 GMT  
		Size: 148.4 MB (148399588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a305dd732c771b772af1d8feba857aec9a57bad33c4ce270ffb377dc4d3504e`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69281d35c29eed55833ecda073b13929c3a92e8d007e1370a0faba21cd47cf1d`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3551e736d7af41dbfeec0530680cf7b2e5185f5845923953e3c863b0cd79a3`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e72c7531ba87c5ea617cb23b9946f906bced95f2510f026e9edbad8dccd870`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c63c870a7cbb46ad13009b82a0f0aa0c3900d67fbf83d371a5e042d06b341a`  
		Last Modified: Sat, 28 Oct 2023 03:56:08 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00a7f96c3e7582bdc61a7da1ce2c4e0dd2677aae82ba0d162e76974c5846d1f`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b77d413ae8139f271405d0a5d3c3baeccf0cb4d1d28ea2642e7d638ae87dd1`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:efc61ce60a9d514a1b062a2b8615309294f71b273b4b7f5b3ce33ef273a36c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:b4c00f3d522ecf35085669952a1e7f8d3bc653c6db8d2ea06745067b7451608b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249278501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7774313fed89667efbcb292dcce4d79ad5a6e1e9fed4140ab8d8047e00642274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 28 Oct 2023 03:50:54 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:51:44 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:51:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:51:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:51:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:51:46 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:51:49 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:51:51 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:51:51 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:51:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:51:52 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:51:52 GMT
USER 1001
# Sat, 28 Oct 2023 03:51:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a605fb25d797064c47be29eb769c24e001d08f5e8d62528c9efe7f6975e29c27`  
		Last Modified: Sat, 28 Oct 2023 03:56:27 GMT  
		Size: 148.4 MB (148399588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a305dd732c771b772af1d8feba857aec9a57bad33c4ce270ffb377dc4d3504e`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69281d35c29eed55833ecda073b13929c3a92e8d007e1370a0faba21cd47cf1d`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3551e736d7af41dbfeec0530680cf7b2e5185f5845923953e3c863b0cd79a3`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e72c7531ba87c5ea617cb23b9946f906bced95f2510f026e9edbad8dccd870`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c63c870a7cbb46ad13009b82a0f0aa0c3900d67fbf83d371a5e042d06b341a`  
		Last Modified: Sat, 28 Oct 2023 03:56:08 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00a7f96c3e7582bdc61a7da1ce2c4e0dd2677aae82ba0d162e76974c5846d1f`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b77d413ae8139f271405d0a5d3c3baeccf0cb4d1d28ea2642e7d638ae87dd1`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:f02537d06a9635684ed241534720ef741be056cbf3d61b4f116bf6583597321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:8d6ab72c7cf21df79f80d6d25b299f7d268cc92ef4e773051116b5ff3eb5f1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272703734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6583aaef0c92ce88a1fdbe8145fa19df67d2cc517cbde2ad84298e2e506cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:49:46 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 28 Oct 2023 03:49:46 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:49:47 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:50:40 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:50:42 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:50:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:50:46 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:50:48 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:50:48 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:50:49 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:50:49 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:50:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:50:49 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:50:49 GMT
USER 1001
# Sat, 28 Oct 2023 03:50:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333bc9d3ee05bf48946f358d4d89fb102321d07b97ebb6b3358e5e232e35e58`  
		Last Modified: Sat, 28 Oct 2023 03:55:57 GMT  
		Size: 171.8 MB (171824816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4354fe6b0af06cec52bdba082495e28d69c2ea57029f41174a320d08294a6dae`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee71068ca0cd8a1a1f1c08f0b09a9d97060be2f6a15c863fe3dccc6f64ecedf1`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9946914dda692502f637e87722e8d95a3a28232493fdc7071063e5107da0ca51`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16953c45b3a1409e51afae93764deace18b0dc66b6b7f535f75d47eb4c972fc`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d922cf67c7ae1a995d7a0eab5101fe6670f5d18b64caa3ec7052c9722617100`  
		Last Modified: Sat, 28 Oct 2023 03:55:36 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ec53cf21ca808e7eaf6c8b97ead7b4703118e24651f104b52deb852f4b79a`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a864e6ad90b15619737435bf369e6a4faad4369ac104f2e85851778987a383`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:f02537d06a9635684ed241534720ef741be056cbf3d61b4f116bf6583597321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:8d6ab72c7cf21df79f80d6d25b299f7d268cc92ef4e773051116b5ff3eb5f1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272703734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6583aaef0c92ce88a1fdbe8145fa19df67d2cc517cbde2ad84298e2e506cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:49:46 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 28 Oct 2023 03:49:46 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:49:47 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:50:40 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:50:42 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:50:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:50:46 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:50:48 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:50:48 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:50:49 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:50:49 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:50:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:50:49 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:50:49 GMT
USER 1001
# Sat, 28 Oct 2023 03:50:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333bc9d3ee05bf48946f358d4d89fb102321d07b97ebb6b3358e5e232e35e58`  
		Last Modified: Sat, 28 Oct 2023 03:55:57 GMT  
		Size: 171.8 MB (171824816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4354fe6b0af06cec52bdba082495e28d69c2ea57029f41174a320d08294a6dae`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee71068ca0cd8a1a1f1c08f0b09a9d97060be2f6a15c863fe3dccc6f64ecedf1`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9946914dda692502f637e87722e8d95a3a28232493fdc7071063e5107da0ca51`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16953c45b3a1409e51afae93764deace18b0dc66b6b7f535f75d47eb4c972fc`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d922cf67c7ae1a995d7a0eab5101fe6670f5d18b64caa3ec7052c9722617100`  
		Last Modified: Sat, 28 Oct 2023 03:55:36 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ec53cf21ca808e7eaf6c8b97ead7b4703118e24651f104b52deb852f4b79a`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a864e6ad90b15619737435bf369e6a4faad4369ac104f2e85851778987a383`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
