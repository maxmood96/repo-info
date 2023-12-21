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
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
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
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.43`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.43-centos`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43-centos` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26-centos`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26-centos` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
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
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.43`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.43` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.34-26`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:eae40ace3716c7b4c7b21095c49064a2c2eb1e5c90843a0cd3379cc979bb786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:a30af127eca3f6a1cf4fe91ad4942be4d69f0310593f52e367d8f544ef2a461d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231936487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621b1d49929319e71c1fdeb403b36fbf6ce3abd590c50b8941d9c018f5a6873c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 20 Dec 2023 23:23:03 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:23:06 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:23:59 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:24:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:24:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:24:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:24:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:24:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:24:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:24:07 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:24:07 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:24:07 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:24:07 GMT
USER 1001
# Wed, 20 Dec 2023 23:24:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcb1e55dc12491ee0b44a4746c329a2dfdd5ff230fa0f103a5d70761523baa0`  
		Last Modified: Wed, 20 Dec 2023 23:26:56 GMT  
		Size: 4.3 MB (4293774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5e769ea5f5fe1fb3f98563d8011e204206a4e4beb0796b1ca7a78f2c6fce54`  
		Last Modified: Wed, 20 Dec 2023 23:27:10 GMT  
		Size: 117.8 MB (117771177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25297c703b81d2e7c57f81a7e8a5e07588da10eaf7aff59fb3666f8eaf0d0f3a`  
		Last Modified: Wed, 20 Dec 2023 23:26:55 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073ee793ba235bff7e41225e6f5d4718f69a950d37e272a03b992aa4ee1a674d`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e48935a1d0a6c83744fc37653baf566c4bda529b2492842a44c7fa4e23635`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a616cb9f129916b2c87a76cd7d48770104314144d803d5bc01bf1a8a1f6fa0bd`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044c09aa9fa7c310857a378cfbdf3481d8dfc1da5431a6970f509799104ddc26`  
		Last Modified: Wed, 20 Dec 2023 23:26:54 GMT  
		Size: 8.2 MB (8151463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800b094dfb4b1465623575baba8552389da2e259d577313640252401589974f`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:eae40ace3716c7b4c7b21095c49064a2c2eb1e5c90843a0cd3379cc979bb786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:a30af127eca3f6a1cf4fe91ad4942be4d69f0310593f52e367d8f544ef2a461d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231936487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621b1d49929319e71c1fdeb403b36fbf6ce3abd590c50b8941d9c018f5a6873c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 20 Dec 2023 23:23:03 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:23:06 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:23:59 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:24:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:24:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:24:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:24:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:24:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:24:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:24:07 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:24:07 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:24:07 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:24:07 GMT
USER 1001
# Wed, 20 Dec 2023 23:24:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcb1e55dc12491ee0b44a4746c329a2dfdd5ff230fa0f103a5d70761523baa0`  
		Last Modified: Wed, 20 Dec 2023 23:26:56 GMT  
		Size: 4.3 MB (4293774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5e769ea5f5fe1fb3f98563d8011e204206a4e4beb0796b1ca7a78f2c6fce54`  
		Last Modified: Wed, 20 Dec 2023 23:27:10 GMT  
		Size: 117.8 MB (117771177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25297c703b81d2e7c57f81a7e8a5e07588da10eaf7aff59fb3666f8eaf0d0f3a`  
		Last Modified: Wed, 20 Dec 2023 23:26:55 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073ee793ba235bff7e41225e6f5d4718f69a950d37e272a03b992aa4ee1a674d`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e48935a1d0a6c83744fc37653baf566c4bda529b2492842a44c7fa4e23635`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a616cb9f129916b2c87a76cd7d48770104314144d803d5bc01bf1a8a1f6fa0bd`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044c09aa9fa7c310857a378cfbdf3481d8dfc1da5431a6970f509799104ddc26`  
		Last Modified: Wed, 20 Dec 2023 23:26:54 GMT  
		Size: 8.2 MB (8151463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800b094dfb4b1465623575baba8552389da2e259d577313640252401589974f`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:93a645d2d71449edbe15cd6588cbb84fb81f05105e795e027c37d4ee399ecaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:98f330c5e3fe26d4752bad2ce8e37935cf411b10ac43340751a9b3098cc5287c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250447997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8208fe15697759e92eda776dd0c889a5d352ad23f31e35a64037ad77a71aa9ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:21:53 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 20 Dec 2023 23:21:53 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:21:53 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 20 Dec 2023 23:21:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:21:53 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:22:48 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:22:49 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:22:49 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:22:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:22:50 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:22:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:22:56 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:22:56 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:22:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:22:56 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 20 Dec 2023 23:22:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:22:57 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:22:57 GMT
USER 1001
# Wed, 20 Dec 2023 23:22:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff7f71304b38ceb03e7ee02f6f7c148673d9c4a5275b1c52f26f5dc78435404`  
		Last Modified: Wed, 20 Dec 2023 23:26:44 GMT  
		Size: 136.3 MB (136283121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e707b6f568e3d9d9ccdea7f5aa94710ba35fcb4eaa27b39e031f0d0cfeb24f63`  
		Last Modified: Wed, 20 Dec 2023 23:26:26 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a2122acb5beea6aa1e2e19f0a370e5e1875eaa95da470c629baef6dc5a082f`  
		Last Modified: Wed, 20 Dec 2023 23:26:26 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42e5cde49019ff10fce7c160016f1cb376c7a11e8c8a05dfccdc516fe2e788d`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa55f99f632d501c7adf4f78a6aeb6f41b97f8e28254a43d4ed48497170c3bd1`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d2f2e1b8d5b6b74ea249a008a316c2c60f51027d411216a9f22b7097cf34e3`  
		Last Modified: Wed, 20 Dec 2023 23:26:25 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a05d64f73634fa93009ea33aac98f0994e5bebc0ff1d40cd7ed07ed843a971`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef6e4000ee72fa7fa4e59f3465da68019c837551fd247d285814bebbe4898c4`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:93a645d2d71449edbe15cd6588cbb84fb81f05105e795e027c37d4ee399ecaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:98f330c5e3fe26d4752bad2ce8e37935cf411b10ac43340751a9b3098cc5287c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250447997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8208fe15697759e92eda776dd0c889a5d352ad23f31e35a64037ad77a71aa9ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:21:53 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 20 Dec 2023 23:21:53 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:21:53 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 20 Dec 2023 23:21:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:21:53 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:22:48 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:22:49 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:22:49 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:22:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:22:50 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:22:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:22:56 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:22:56 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:22:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:22:56 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 20 Dec 2023 23:22:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:22:57 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:22:57 GMT
USER 1001
# Wed, 20 Dec 2023 23:22:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff7f71304b38ceb03e7ee02f6f7c148673d9c4a5275b1c52f26f5dc78435404`  
		Last Modified: Wed, 20 Dec 2023 23:26:44 GMT  
		Size: 136.3 MB (136283121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e707b6f568e3d9d9ccdea7f5aa94710ba35fcb4eaa27b39e031f0d0cfeb24f63`  
		Last Modified: Wed, 20 Dec 2023 23:26:26 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a2122acb5beea6aa1e2e19f0a370e5e1875eaa95da470c629baef6dc5a082f`  
		Last Modified: Wed, 20 Dec 2023 23:26:26 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42e5cde49019ff10fce7c160016f1cb376c7a11e8c8a05dfccdc516fe2e788d`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa55f99f632d501c7adf4f78a6aeb6f41b97f8e28254a43d4ed48497170c3bd1`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d2f2e1b8d5b6b74ea249a008a316c2c60f51027d411216a9f22b7097cf34e3`  
		Last Modified: Wed, 20 Dec 2023 23:26:25 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a05d64f73634fa93009ea33aac98f0994e5bebc0ff1d40cd7ed07ed843a971`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef6e4000ee72fa7fa4e59f3465da68019c837551fd247d285814bebbe4898c4`  
		Last Modified: Wed, 20 Dec 2023 23:26:24 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:70815eb28601ea64bf26fe10e44aefe21f63aeb2a05067a58a9457ffc163d9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:8adb46090f8725e72bdeef28d32d59cb5d9e3c9fd208de1dd389f706c2a49ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263055134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12793e251586d3ec640a6b154248096327533e3c0122d383c3f6a5e237ccf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 20 Dec 2023 23:20:43 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:21:39 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:21:40 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:21:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:21:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:21:41 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:21:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:21:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:21:47 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:21:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:21:47 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:21:47 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:21:48 GMT
USER 1001
# Wed, 20 Dec 2023 23:21:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ad04f12bc98662f152950972d761ce282519815a59132dec61b4f96de24c7`  
		Last Modified: Wed, 20 Dec 2023 23:26:14 GMT  
		Size: 148.9 MB (148890251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba97b3d77c782017bf9c3471a6131a76b243b3ea66d3cc8d7ea0703c461c170`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601453f10a5c6118ab5f86a2a6eb8050463de3d60a76dd3367b43e28f70d1eb5`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4017d4aec5d279b15c8b11c6e851678cf75e966ae5afe8b4429a6e388250010e`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43d69aad92641bbb56efe2a9a00636aaed595762ab8628d09b19c694b3a7db`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece106b3b8646f991a0d770aa326708ee85be2e854cef830407e8b79b1568cf`  
		Last Modified: Wed, 20 Dec 2023 23:25:54 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398eb3641f6a7fc57809d9ff6dd1603c75a49adc789f8cd17cb78a484f8fbb1a`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760bed2f1396884ac9ded362d1e39aeef9b1cb71d366bbd9e6cf75126424587f`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:70815eb28601ea64bf26fe10e44aefe21f63aeb2a05067a58a9457ffc163d9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:8adb46090f8725e72bdeef28d32d59cb5d9e3c9fd208de1dd389f706c2a49ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263055134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12793e251586d3ec640a6b154248096327533e3c0122d383c3f6a5e237ccf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 20 Dec 2023 23:20:43 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:21:39 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:21:40 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:21:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:21:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:21:41 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:21:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:21:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:21:47 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:21:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:21:47 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:21:47 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:21:48 GMT
USER 1001
# Wed, 20 Dec 2023 23:21:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ad04f12bc98662f152950972d761ce282519815a59132dec61b4f96de24c7`  
		Last Modified: Wed, 20 Dec 2023 23:26:14 GMT  
		Size: 148.9 MB (148890251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba97b3d77c782017bf9c3471a6131a76b243b3ea66d3cc8d7ea0703c461c170`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601453f10a5c6118ab5f86a2a6eb8050463de3d60a76dd3367b43e28f70d1eb5`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4017d4aec5d279b15c8b11c6e851678cf75e966ae5afe8b4429a6e388250010e`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43d69aad92641bbb56efe2a9a00636aaed595762ab8628d09b19c694b3a7db`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece106b3b8646f991a0d770aa326708ee85be2e854cef830407e8b79b1568cf`  
		Last Modified: Wed, 20 Dec 2023 23:25:54 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398eb3641f6a7fc57809d9ff6dd1603c75a49adc789f8cd17cb78a484f8fbb1a`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760bed2f1396884ac9ded362d1e39aeef9b1cb71d366bbd9e6cf75126424587f`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:ac94798e688a1a3f0209524699bb2c205665bce7168aa8f3943c00c13b8f15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:78c653fd0d857bd52d487a0421709339fa21cd9956a61a90b3e597f266dff1da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286532162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bef21bd6762406c5351fcef47dc1a3150f6e81366ddad5557cef700af28e022`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 20 Dec 2023 23:19:23 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:20:20 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:20:22 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:20:22 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:20:23 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:20:23 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:20:26 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:20:29 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:20:29 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:20:30 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:20:30 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:20:30 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:20:30 GMT
USER 1001
# Wed, 20 Dec 2023 23:20:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1cfb46a32b7f116e140080c70bae94ede67a054ec8ca19013a1c3f03ac9b21`  
		Last Modified: Wed, 20 Dec 2023 23:25:43 GMT  
		Size: 172.4 MB (172367277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d4f387c0345e73df260fff0f0fcd157acf4d194e45081eef3cc2752b8f034`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd1df821ac6601ddd4f88facccf2f8d9918eccf19d97d4fd9975487041dc26`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79739b5162133568d02868e8474cd2a5b7a88dce69345fcb86d0978e558bbf`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c838e4c91d51625d47934536de12bdb97011d852555b715474de3ae408667a59`  
		Last Modified: Wed, 20 Dec 2023 23:25:20 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5b08c83667cd05d1ba39f3ae01f7a2e40ab1dbf1c82be4361e186d3018cb7e`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0310c1458b09e6718a8f9419f053daac5257e3c76da0f306786c3b427951bc1`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1022828e0c9b54f5448648a480cc757451bd1a13c4c79f94c7604052c1447d3`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:ac94798e688a1a3f0209524699bb2c205665bce7168aa8f3943c00c13b8f15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:78c653fd0d857bd52d487a0421709339fa21cd9956a61a90b3e597f266dff1da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286532162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bef21bd6762406c5351fcef47dc1a3150f6e81366ddad5557cef700af28e022`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 20 Dec 2023 23:19:23 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:20:20 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:20:22 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:20:22 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:20:23 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:20:23 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:20:26 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:20:29 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:20:29 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:20:30 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:20:30 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:20:30 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:20:30 GMT
USER 1001
# Wed, 20 Dec 2023 23:20:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1cfb46a32b7f116e140080c70bae94ede67a054ec8ca19013a1c3f03ac9b21`  
		Last Modified: Wed, 20 Dec 2023 23:25:43 GMT  
		Size: 172.4 MB (172367277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d4f387c0345e73df260fff0f0fcd157acf4d194e45081eef3cc2752b8f034`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd1df821ac6601ddd4f88facccf2f8d9918eccf19d97d4fd9975487041dc26`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79739b5162133568d02868e8474cd2a5b7a88dce69345fcb86d0978e558bbf`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c838e4c91d51625d47934536de12bdb97011d852555b715474de3ae408667a59`  
		Last Modified: Wed, 20 Dec 2023 23:25:20 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5b08c83667cd05d1ba39f3ae01f7a2e40ab1dbf1c82be4361e186d3018cb7e`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0310c1458b09e6718a8f9419f053daac5257e3c76da0f306786c3b427951bc1`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1022828e0c9b54f5448648a480cc757451bd1a13c4c79f94c7604052c1447d3`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
