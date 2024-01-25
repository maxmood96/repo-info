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
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
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
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.43`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.43-centos`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.43-centos` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.34-26-centos`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.34-26-centos` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
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
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.43`

```console
$ docker pull percona@sha256:0e381d769192752775058d33090b57c3bbf8c346b5f6f2caca7fd15f151f6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.43` - linux; amd64

```console
$ docker pull percona@sha256:1a21908a07a83b28fae3321cd0d5a9a43a70c2ab61e519a99172cd869acc9d1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453127382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0b154159969db7762db0e0aaa9140829bc4917256fb724411057777856870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 17 Jan 2024 21:55:35 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 17 Jan 2024 21:55:35 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:55:35 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 17 Jan 2024 21:56:15 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:56:17 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 17 Jan 2024 21:56:17 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:56:17 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:56:18 GMT
USER mysql
# Wed, 17 Jan 2024 21:56:18 GMT
EXPOSE 3306
# Wed, 17 Jan 2024 21:56:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7a17c2ab16fb2f9b2754dd4819c1aee4e81f3f2bb942e3c2d07827bc79284a`  
		Last Modified: Wed, 17 Jan 2024 22:03:14 GMT  
		Size: 138.2 MB (138161059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f5d2832e4054178a9f62c000da6f55b3fb6b8ae20f159b566f15a80791230f`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f26d8ce7c07556b15fa1ee7c3b77b2195aabd87ea2f0f7d1ee262e753587962`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.34-26`

```console
$ docker pull percona@sha256:47edee23f4514e24eb7c834e74ece499f9760e3066f1c09e674cce7ba6f923cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.34-26` - linux; amd64

```console
$ docker pull percona@sha256:e6db5c7cc15b5f156e363f212645e318b22fa00a2e6f8b9193f5b279b1471519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394625410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b3b4705b482f4279f9ee58d15de2ad22109266dec9b34e3c80a886b5d56cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Jan 2024 04:03:12 GMT
ADD file:b6649b3938106175355e394f455963ceb2a6251bd95aeea0b2e6c49858d887bb in / 
# Thu, 25 Jan 2024 04:03:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 04:35:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Jan 2024 04:35:04 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 25 Jan 2024 04:35:04 GMT
ENV OS_VER=el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 25 Jan 2024 04:35:04 GMT
ENV PS_REPO=release
# Thu, 25 Jan 2024 04:35:07 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Jan 2024 04:36:13 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 04:36:18 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Jan 2024 04:36:18 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 04:36:18 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 04:36:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 04:36:18 GMT
USER mysql
# Thu, 25 Jan 2024 04:36:18 GMT
EXPOSE 3306 33060
# Thu, 25 Jan 2024 04:36:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d3de9e1d014beafdb84e4e55cafe57e7b775e3e66caabc3a2e3b335fee18d785`  
		Last Modified: Thu, 25 Jan 2024 04:04:34 GMT  
		Size: 95.1 MB (95139965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c678a83453f38db9d0a0c2cf90f4aa81da53039726c7cba13c317e80ee1ff`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ff67432ba14225af1b86f90e11704723947d3443bcf49d1c561b47e4f0c74`  
		Last Modified: Thu, 25 Jan 2024 04:36:58 GMT  
		Size: 7.3 MB (7284758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de57e79d30018002c3aa8bf1727f119b99b20ca909fc20cb636ccd7ab5d1756`  
		Last Modified: Thu, 25 Jan 2024 04:37:39 GMT  
		Size: 292.2 MB (292194805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91b0acb51f71ef545a4db6a35024fad3437e803b1009b8b198fe1397ffad8`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1abc35be80f276459c73da0a2c5663fae4d75728b1533cca5e820b563db62a`  
		Last Modified: Thu, 25 Jan 2024 04:36:57 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:2356ba75ee394c9a72aeaa4980e5d52d562fc76fbeb82dec7ca31c1aa643696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:b967d8c94d2b3bcd428348bd5e996aaa767066c72b46cb440a08cc82d88cb094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231930783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825d8de20a36962acd69548cec089b6c8233df7b5b9be68e3e4377867ba9d81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 17 Jan 2024 22:00:19 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 22:00:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 22:01:16 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 22:01:17 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 22:01:17 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 22:01:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 22:01:17 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 22:01:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 22:01:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 22:01:23 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 22:01:23 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 17 Jan 2024 22:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 22:01:23 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 22:01:23 GMT
USER 1001
# Wed, 17 Jan 2024 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f632f2bd87095102ec7489275b3507016e06a1ea2cb462e9877e6188dd9186`  
		Last Modified: Wed, 17 Jan 2024 22:05:25 GMT  
		Size: 4.3 MB (4290064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4845a90d8eb1405d1ec3211d3110036a15d205f20d8fcd2b48dd2c452cee55b4`  
		Last Modified: Wed, 17 Jan 2024 22:05:40 GMT  
		Size: 117.8 MB (117768583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7571a5609c702ff5d51f9869eb97a8e5420d76fbb6b582b9e23aad0d9d6a6322`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b6bc9254fc6a89085a5923f8a018ca1a5e2a18ec5ecf4a158ae5fd9dde81b`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a00c1feb8da5941a892f1362bc863e44428494cf861357eda233822480b6d`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c070b9c3f407e3b5d1b855278c8c1fee561d4d2d10cc3a4f73bffe60eeeed1ea`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315474d99ca5f5783af3ba85b780e4f424f10af0883a59b2a6022a300086651f`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 8.2 MB (8151447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539d5cfbbc4b099ba959d2fcb2ebbe0b4753695aaa61cac872ba3b0754f2608`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:2356ba75ee394c9a72aeaa4980e5d52d562fc76fbeb82dec7ca31c1aa643696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:b967d8c94d2b3bcd428348bd5e996aaa767066c72b46cb440a08cc82d88cb094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231930783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825d8de20a36962acd69548cec089b6c8233df7b5b9be68e3e4377867ba9d81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 17 Jan 2024 22:00:19 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 22:00:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 22:01:16 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 22:01:17 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 22:01:17 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 22:01:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 22:01:17 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 22:01:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 22:01:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 22:01:23 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 22:01:23 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 17 Jan 2024 22:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 22:01:23 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 22:01:23 GMT
USER 1001
# Wed, 17 Jan 2024 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f632f2bd87095102ec7489275b3507016e06a1ea2cb462e9877e6188dd9186`  
		Last Modified: Wed, 17 Jan 2024 22:05:25 GMT  
		Size: 4.3 MB (4290064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4845a90d8eb1405d1ec3211d3110036a15d205f20d8fcd2b48dd2c452cee55b4`  
		Last Modified: Wed, 17 Jan 2024 22:05:40 GMT  
		Size: 117.8 MB (117768583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7571a5609c702ff5d51f9869eb97a8e5420d76fbb6b582b9e23aad0d9d6a6322`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b6bc9254fc6a89085a5923f8a018ca1a5e2a18ec5ecf4a158ae5fd9dde81b`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a00c1feb8da5941a892f1362bc863e44428494cf861357eda233822480b6d`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c070b9c3f407e3b5d1b855278c8c1fee561d4d2d10cc3a4f73bffe60eeeed1ea`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315474d99ca5f5783af3ba85b780e4f424f10af0883a59b2a6022a300086651f`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 8.2 MB (8151447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539d5cfbbc4b099ba959d2fcb2ebbe0b4753695aaa61cac872ba3b0754f2608`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:21e629316e847395a52c7841ee0d34d0b47e840113db6c4de9a3b92d66090d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:9832f94eb9d74a3c70cdfc2782f77d5f4fd4530d17752736ee65c361800853cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250447219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45faf5f2b11286bf670cb45c852375ff0285e945298996c0234faac7b2eb1412`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:59:09 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 17 Jan 2024 21:59:09 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:59:09 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 17 Jan 2024 21:59:09 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:59:09 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 22:00:04 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 22:00:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 22:00:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 22:00:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 22:00:06 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 22:00:10 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 22:00:12 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 22:00:13 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 22:00:13 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 22:00:13 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 17 Jan 2024 22:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 22:00:14 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 22:00:14 GMT
USER 1001
# Wed, 17 Jan 2024 22:00:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37f6bdaa25be9a7fb8e5a7088b85eff7c67aa6272fbbb2a47632731ec6ef84`  
		Last Modified: Wed, 17 Jan 2024 22:05:04 GMT  
		Size: 136.3 MB (136285365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbaae02ad66dc3fe9c434c4dac284b62b78b8d4f2d6933fe21340e042fa512e`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ad9cd3bb3ba5438708f6039901870ea06b329f2fadd89757920931289beb3`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec4abaf83354220851dbc7626fd5ded6ca1ccbf0e4601c0e6487709e68ddfca`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf59abfe925b4e7839a6233c396808f3338ae516ad30c2478ed7193dbcd7272`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d9720d98574176589f688918729a479664ff46852d327dc9f4211454f9db4`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031c0894baa0eddfd0b7227e59c252a8c20f9326b968adc10dab748a88b4d2f0`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c703a299310f62a1dbb7222a16267faf20c411a5f3a8235defb407921dc0ad90`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:21e629316e847395a52c7841ee0d34d0b47e840113db6c4de9a3b92d66090d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:9832f94eb9d74a3c70cdfc2782f77d5f4fd4530d17752736ee65c361800853cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250447219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45faf5f2b11286bf670cb45c852375ff0285e945298996c0234faac7b2eb1412`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:59:09 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 17 Jan 2024 21:59:09 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:59:09 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 17 Jan 2024 21:59:09 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:59:09 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 22:00:04 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 22:00:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 22:00:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 22:00:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 22:00:06 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 22:00:10 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 22:00:12 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 22:00:13 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 22:00:13 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 22:00:13 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 17 Jan 2024 22:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 22:00:14 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 22:00:14 GMT
USER 1001
# Wed, 17 Jan 2024 22:00:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37f6bdaa25be9a7fb8e5a7088b85eff7c67aa6272fbbb2a47632731ec6ef84`  
		Last Modified: Wed, 17 Jan 2024 22:05:04 GMT  
		Size: 136.3 MB (136285365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbaae02ad66dc3fe9c434c4dac284b62b78b8d4f2d6933fe21340e042fa512e`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ad9cd3bb3ba5438708f6039901870ea06b329f2fadd89757920931289beb3`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec4abaf83354220851dbc7626fd5ded6ca1ccbf0e4601c0e6487709e68ddfca`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf59abfe925b4e7839a6233c396808f3338ae516ad30c2478ed7193dbcd7272`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031d9720d98574176589f688918729a479664ff46852d327dc9f4211454f9db4`  
		Last Modified: Wed, 17 Jan 2024 22:04:46 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031c0894baa0eddfd0b7227e59c252a8c20f9326b968adc10dab748a88b4d2f0`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c703a299310f62a1dbb7222a16267faf20c411a5f3a8235defb407921dc0ad90`  
		Last Modified: Wed, 17 Jan 2024 22:04:44 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:dc14ebf9c82ee3efb539c0b30d32ae8b16c3bdfba53e22216136c2459ac22573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:e5daf1e26140cc7ad848d75c16ae13d5a8fc3264c614a5f964953645e4ba799c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263059304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228fca6a3426bf421cb9a37922b93aab9bd650a9981849d610f6e04f2679e64c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 17 Jan 2024 21:57:59 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:58:55 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:58:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:58:57 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:58:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:58:57 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:59:00 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:59:03 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:59:03 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:59:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:59:04 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:59:04 GMT
USER 1001
# Wed, 17 Jan 2024 21:59:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe51feaec667b43ebe4dbfa80ebf39462ae91c8cb762c847c5c64e2648eac89`  
		Last Modified: Wed, 17 Jan 2024 22:04:34 GMT  
		Size: 148.9 MB (148897448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f581e8d7abb24eac952ccbc4f838541c16fb860289e088a017bd23630b3dc`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030acdccff6cd64780b49f4c9dec9703a09736c19fc281b4c87a61a7ee83fb2`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da24fdeb58cb63596dd3c67daf1a98d79a4ba2c12f59bd25dc108c53283e6a30`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5ab8d3b7cfc45f9c89f455527442657bb537fce12cf24dbb9f65f228679576`  
		Last Modified: Wed, 17 Jan 2024 22:04:15 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c332acb2fb3080151afe9ce0347265aa6a817c8dea9d6a2952e8266e071916c`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa308b191c79311c5cc72ebbcb0afed96ea1cb6efff761e14513eff9aaf27c`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5148a44cc5def52f5cc0a922756c6971799032b9eb5629701026c36423b8ac`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:dc14ebf9c82ee3efb539c0b30d32ae8b16c3bdfba53e22216136c2459ac22573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:e5daf1e26140cc7ad848d75c16ae13d5a8fc3264c614a5f964953645e4ba799c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263059304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228fca6a3426bf421cb9a37922b93aab9bd650a9981849d610f6e04f2679e64c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 17 Jan 2024 21:57:59 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:58:55 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:58:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:58:57 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:58:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:58:57 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:59:00 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:59:03 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:59:03 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:59:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:59:04 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:59:04 GMT
USER 1001
# Wed, 17 Jan 2024 21:59:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe51feaec667b43ebe4dbfa80ebf39462ae91c8cb762c847c5c64e2648eac89`  
		Last Modified: Wed, 17 Jan 2024 22:04:34 GMT  
		Size: 148.9 MB (148897448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f581e8d7abb24eac952ccbc4f838541c16fb860289e088a017bd23630b3dc`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030acdccff6cd64780b49f4c9dec9703a09736c19fc281b4c87a61a7ee83fb2`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da24fdeb58cb63596dd3c67daf1a98d79a4ba2c12f59bd25dc108c53283e6a30`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5ab8d3b7cfc45f9c89f455527442657bb537fce12cf24dbb9f65f228679576`  
		Last Modified: Wed, 17 Jan 2024 22:04:15 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c332acb2fb3080151afe9ce0347265aa6a817c8dea9d6a2952e8266e071916c`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa308b191c79311c5cc72ebbcb0afed96ea1cb6efff761e14513eff9aaf27c`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5148a44cc5def52f5cc0a922756c6971799032b9eb5629701026c36423b8ac`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:3ed58ce8c8fbd69f6c40f0c2f2a5391400ac0d6ad1dec38f8d0a988507f4341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:c61c0c1f807b2f4a839695d2645487f32902dbf6392069f54952e5d94a61b700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6886eab894542f664fb16365fd78e6c669272e6f0f9f43afd566daa836e39450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:56:37 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 17 Jan 2024 21:56:37 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:56:38 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:57:36 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:57:38 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:57:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:57:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:57:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:57:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:57:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:57:46 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:57:46 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:57:46 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:57:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:57:47 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:57:47 GMT
USER 1001
# Wed, 17 Jan 2024 21:57:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc784f65efa9401ff4011d96ad61843e3e829ef0684da656d50275f81fd7b891`  
		Last Modified: Wed, 17 Jan 2024 22:04:05 GMT  
		Size: 172.4 MB (172364605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ccc3bec8e8099f939588998b9513a1404208c34aa0740d98314c064426346e`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071f0596220e5ec25a687c3d55058df77bfb28b16134d9b49ed15764dd95507a`  
		Last Modified: Wed, 17 Jan 2024 22:03:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33f3971df81bf288f8e208e6e7a4bd680e66af4afe884031b2f19eaebc3c3ce`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dfc925e3c4728141cdb40f74115cf372bab06f4ba051e5e431a2854aa8a7c8`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a8e15568d9b9424d8319112f629e1bd1252eb7d29cb4388f198f3066d9074`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48687772c3aa6fdd9acfa90e3f186062c17abdcc545ed79536c7af96f57bec1e`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de666f145043fdebef298bb8cb09c8c78e55c71be85901be57edabfdb4539cb`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:3ed58ce8c8fbd69f6c40f0c2f2a5391400ac0d6ad1dec38f8d0a988507f4341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:c61c0c1f807b2f4a839695d2645487f32902dbf6392069f54952e5d94a61b700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6886eab894542f664fb16365fd78e6c669272e6f0f9f43afd566daa836e39450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:56:37 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 17 Jan 2024 21:56:37 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:56:38 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:57:36 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:57:38 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:57:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:57:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:57:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:57:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:57:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:57:46 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:57:46 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:57:46 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:57:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:57:47 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:57:47 GMT
USER 1001
# Wed, 17 Jan 2024 21:57:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc784f65efa9401ff4011d96ad61843e3e829ef0684da656d50275f81fd7b891`  
		Last Modified: Wed, 17 Jan 2024 22:04:05 GMT  
		Size: 172.4 MB (172364605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ccc3bec8e8099f939588998b9513a1404208c34aa0740d98314c064426346e`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071f0596220e5ec25a687c3d55058df77bfb28b16134d9b49ed15764dd95507a`  
		Last Modified: Wed, 17 Jan 2024 22:03:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33f3971df81bf288f8e208e6e7a4bd680e66af4afe884031b2f19eaebc3c3ce`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dfc925e3c4728141cdb40f74115cf372bab06f4ba051e5e431a2854aa8a7c8`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a8e15568d9b9424d8319112f629e1bd1252eb7d29cb4388f198f3066d9074`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48687772c3aa6fdd9acfa90e3f186062c17abdcc545ed79536c7af96f57bec1e`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de666f145043fdebef298bb8cb09c8c78e55c71be85901be57edabfdb4539cb`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
