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
-	[`percona:5.7.39`](#percona5739)
-	[`percona:5.7.39-centos`](#percona5739-centos)
-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.33-25`](#percona8033-25)
-	[`percona:8.0.33-25-centos`](#percona8033-25-centos)
-	[`percona:centos`](#perconacentos)
-	[`percona:ps-5`](#perconaps-5)
-	[`percona:ps-5.6`](#perconaps-56)
-	[`percona:ps-5.6.51-2`](#perconaps-5651-2)
-	[`percona:ps-5.7`](#perconaps-57)
-	[`percona:ps-5.7.39`](#perconaps-5739)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.33-25`](#perconaps-8033-25)
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
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
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
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.39`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.39` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.39-centos`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.39-centos` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.33-25`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.33-25` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.33-25-centos`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.33-25-centos` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
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
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.39`

```console
$ docker pull percona@sha256:0cbb807c3de82e1bc763f00ff8b633290875f4076f69ea6c989ab515cfcbe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.39` - linux; amd64

```console
$ docker pull percona@sha256:2a8e479a7e459c61ad64831d91910879a4af05e2f04ac433b88ea11dde289b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421034463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8bf4607165d6bc23f1b6b3e121b5a2b46d5a8b7df7679313f1b1aeb03515b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:43:11 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:43:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 11 Aug 2023 01:43:45 GMT
ENV PS_VERSION=5.7.39-42.1
# Fri, 11 Aug 2023 01:43:45 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:43:45 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Fri, 11 Aug 2023 01:44:22 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:44:24 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 11 Aug 2023 01:44:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:44:24 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:44:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:44:24 GMT
USER mysql
# Fri, 11 Aug 2023 01:44:24 GMT
EXPOSE 3306
# Fri, 11 Aug 2023 01:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b0dc9cd2751a3539365ab7ba69b88d49e2e368fd2527795ea9d30b41dc138b`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c18f93896a6a118da854e09e1fac2e23f9cb990d5877c2ba725dba6ffc81f`  
		Last Modified: Fri, 11 Aug 2023 01:50:35 GMT  
		Size: 194.6 MB (194562765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27051cd22cf3dc83258f5dddf31aec197164a2cd54fa2088d146aab4a7ca7abb`  
		Last Modified: Fri, 11 Aug 2023 01:50:43 GMT  
		Size: 137.5 MB (137543591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d198a51b2178a015c1ad39ddfee2d4d85178f22cb69618197a325cc650063f`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c956242ebd65b10de148c1917b56b4311d6a00acf4c35ec49c46dc1d3749d`  
		Last Modified: Fri, 11 Aug 2023 01:50:25 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.33-25`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.33-25` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:32d6bd395d9c17bed76c0f30faa337d758544608fb610e5449538bc8701d71cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:d8bb4132f25c09027aca57aaec8d4d9b01a8cdac007b67147b9bf757c620e2a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219064726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137675a39565e1fd389f0c154c1cbdce18ef58efbb379d22f174b4bee5652b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:48:06 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 11 Aug 2023 01:48:06 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:48:06 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 11 Aug 2023 01:48:07 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:48:07 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:48:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:48:55 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:48:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:48:56 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:48:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:48:57 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:48:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:49:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:49:02 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:49:02 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:49:02 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:49:02 GMT
USER 1001
# Fri, 11 Aug 2023 01:49:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf57b5315533d0ec287f46200a45f69284fdc93e647d9c28be2760714547ae9`  
		Last Modified: Fri, 11 Aug 2023 01:52:39 GMT  
		Size: 3.8 MB (3797086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4951e68cce62765eaba32e9f575f22b69c1489ddf6bf3403921f3d98af263d8`  
		Last Modified: Fri, 11 Aug 2023 01:52:53 GMT  
		Size: 117.3 MB (117258280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5202cacfbc3cf668e909205e857a3b95f74bb5b0780ade9705f761db75d07d4`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc85ba2d940913944c2f44c16f51dc037bcb1991b60b2dcef00ea213b2331a`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee321fffbfeb24e4f4ad6a8c2192f13a623d9ee436c7a3c28c7f098187d15dcd`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e3d3690e050cb7e46f835d5381f9957bd2226b1f55c5cd4348d03576b5353`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c790b461021fbb20eaa94d3ca96d714c6f52c942b2adccb52c4c2a93f2bf250`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64ceccb71d3b7f3a22ee4f32d157c1cf568b5cad903fdb46d0742510268ad53`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:32d6bd395d9c17bed76c0f30faa337d758544608fb610e5449538bc8701d71cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:d8bb4132f25c09027aca57aaec8d4d9b01a8cdac007b67147b9bf757c620e2a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219064726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137675a39565e1fd389f0c154c1cbdce18ef58efbb379d22f174b4bee5652b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:48:06 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 11 Aug 2023 01:48:06 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:48:06 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 11 Aug 2023 01:48:07 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:48:07 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:48:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:48:55 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:48:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:48:56 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:48:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:48:57 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:48:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:49:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:49:02 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:49:02 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:49:02 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:49:02 GMT
USER 1001
# Fri, 11 Aug 2023 01:49:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf57b5315533d0ec287f46200a45f69284fdc93e647d9c28be2760714547ae9`  
		Last Modified: Fri, 11 Aug 2023 01:52:39 GMT  
		Size: 3.8 MB (3797086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4951e68cce62765eaba32e9f575f22b69c1489ddf6bf3403921f3d98af263d8`  
		Last Modified: Fri, 11 Aug 2023 01:52:53 GMT  
		Size: 117.3 MB (117258280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5202cacfbc3cf668e909205e857a3b95f74bb5b0780ade9705f761db75d07d4`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc85ba2d940913944c2f44c16f51dc037bcb1991b60b2dcef00ea213b2331a`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee321fffbfeb24e4f4ad6a8c2192f13a623d9ee436c7a3c28c7f098187d15dcd`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e3d3690e050cb7e46f835d5381f9957bd2226b1f55c5cd4348d03576b5353`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c790b461021fbb20eaa94d3ca96d714c6f52c942b2adccb52c4c2a93f2bf250`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64ceccb71d3b7f3a22ee4f32d157c1cf568b5cad903fdb46d0742510268ad53`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:082ecf5036913659bd1143a8698fcc426c394e184d8a73d8944f82e950991fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:c2e64144aa3e71c779a2ce42fa17e25f6d89029bd6246630dff01fa383288097
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204fa5281e1c7cefbc78a152995e2699c11be7f966a9dbcc27392f92590fd92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:46:56 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 11 Aug 2023 01:46:56 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:46:56 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 11 Aug 2023 01:46:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:46:57 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:47:45 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:47:46 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:47:46 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:47:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:47:46 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:47:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:47:52 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:47:52 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 11 Aug 2023 01:47:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:47:52 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:47:53 GMT
USER 1001
# Fri, 11 Aug 2023 01:47:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef92b1ab4af34b9b3cf9ed5057a7a90e47b7d300eccc205c9ec7515e2dec5fb7`  
		Last Modified: Fri, 11 Aug 2023 01:52:28 GMT  
		Size: 135.8 MB (135798666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0314a478ded2fd7a42b9e3ab0495ef3905f8d1837ce28a990947db02d6198522`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f13bb9d4fb516c8ab6490885acacf10072d05b2ccddd23cda042255f5b919`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f952409a9d1848b70ded12c6741f7178665afbf2bb255d87ec9e38b189277`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158348ee2cc49aae27a3cdd3baf9260087b5a973479a044e6e7c8d4c85ab9290`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d15bc47e848c151e59ae10176b60e4441522a215517b30f875a6b5fab34496`  
		Last Modified: Fri, 11 Aug 2023 01:52:10 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea22b2156f6235633ecd91f31ac7ea06c2a0e7b396a08ff145536bb311c956`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dba217798745766c79c0548c8864ef668d86839137c46678dc7049dd45276f4`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:082ecf5036913659bd1143a8698fcc426c394e184d8a73d8944f82e950991fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:c2e64144aa3e71c779a2ce42fa17e25f6d89029bd6246630dff01fa383288097
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204fa5281e1c7cefbc78a152995e2699c11be7f966a9dbcc27392f92590fd92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:46:56 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 11 Aug 2023 01:46:56 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:46:56 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 11 Aug 2023 01:46:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:46:57 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:47:45 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:47:46 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:47:46 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:47:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:47:46 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:47:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:47:52 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:47:52 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 11 Aug 2023 01:47:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:47:52 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:47:53 GMT
USER 1001
# Fri, 11 Aug 2023 01:47:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef92b1ab4af34b9b3cf9ed5057a7a90e47b7d300eccc205c9ec7515e2dec5fb7`  
		Last Modified: Fri, 11 Aug 2023 01:52:28 GMT  
		Size: 135.8 MB (135798666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0314a478ded2fd7a42b9e3ab0495ef3905f8d1837ce28a990947db02d6198522`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f13bb9d4fb516c8ab6490885acacf10072d05b2ccddd23cda042255f5b919`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f952409a9d1848b70ded12c6741f7178665afbf2bb255d87ec9e38b189277`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158348ee2cc49aae27a3cdd3baf9260087b5a973479a044e6e7c8d4c85ab9290`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d15bc47e848c151e59ae10176b60e4441522a215517b30f875a6b5fab34496`  
		Last Modified: Fri, 11 Aug 2023 01:52:10 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea22b2156f6235633ecd91f31ac7ea06c2a0e7b396a08ff145536bb311c956`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dba217798745766c79c0548c8864ef668d86839137c46678dc7049dd45276f4`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:5a1de090b0448263cf215138cffd0d39402aa9b03490092a94e07519cc3c928a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:59155aaac905d912b1d6e98f214398a76198d90c76d9925f4a6fd3ff35d0be96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250211790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62357e193feee44d42dd47665244bc10828fa151526fb1621c30d66351c38c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:45:46 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 11 Aug 2023 01:45:46 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:45:46 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 11 Aug 2023 01:45:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:45:47 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:46:35 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:46:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:46:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:46:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:46:37 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:46:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:46:42 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:46:43 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:46:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:46:43 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:46:43 GMT
USER 1001
# Fri, 11 Aug 2023 01:46:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc588820011bf0f3cde96b16eca92b7b569dc2093158ff0a32b29e5d8ffa91f`  
		Last Modified: Fri, 11 Aug 2023 01:52:00 GMT  
		Size: 148.4 MB (148405672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63425b2f2a086802849440590bb47a5888afa2ae45c5eee7aacf883a7257cef`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bc9c20319e3fb7fdb4d3f577f1c23133effa56861776395616cefd0b870d2d`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352941f34f632dfa06398b346dfe4c8e71dac13baf34d1a18d007c77f72f6676`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30558d227cd0bf4af5e4fb06c86b0be9c5792242f6269d963f301b435bba68b`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bda32ef50d2663304ecc3b265f024b9e41c26a9c5c73513da5e5ca71e345a16`  
		Last Modified: Fri, 11 Aug 2023 01:51:41 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2194b9ab828b8216d95f409f71b585ce9c87942284db5d0bf64ebdd2dd8105`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ed082ab48dcb8171455796e00fc80412fe87b2495e33615c934ba548deb16d`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:5a1de090b0448263cf215138cffd0d39402aa9b03490092a94e07519cc3c928a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:59155aaac905d912b1d6e98f214398a76198d90c76d9925f4a6fd3ff35d0be96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250211790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62357e193feee44d42dd47665244bc10828fa151526fb1621c30d66351c38c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:45:46 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 11 Aug 2023 01:45:46 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:45:46 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 11 Aug 2023 01:45:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:45:47 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:46:35 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:46:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:46:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:46:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:46:37 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:46:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:46:42 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:46:43 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:46:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:46:43 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:46:43 GMT
USER 1001
# Fri, 11 Aug 2023 01:46:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc588820011bf0f3cde96b16eca92b7b569dc2093158ff0a32b29e5d8ffa91f`  
		Last Modified: Fri, 11 Aug 2023 01:52:00 GMT  
		Size: 148.4 MB (148405672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63425b2f2a086802849440590bb47a5888afa2ae45c5eee7aacf883a7257cef`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bc9c20319e3fb7fdb4d3f577f1c23133effa56861776395616cefd0b870d2d`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352941f34f632dfa06398b346dfe4c8e71dac13baf34d1a18d007c77f72f6676`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30558d227cd0bf4af5e4fb06c86b0be9c5792242f6269d963f301b435bba68b`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bda32ef50d2663304ecc3b265f024b9e41c26a9c5c73513da5e5ca71e345a16`  
		Last Modified: Fri, 11 Aug 2023 01:51:41 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2194b9ab828b8216d95f409f71b585ce9c87942284db5d0bf64ebdd2dd8105`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ed082ab48dcb8171455796e00fc80412fe87b2495e33615c934ba548deb16d`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:dfcff956c1450b989317e7f3c51a528688d012d9273d6a02f27945b9981befc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:8d16ac171b620f61410200cf4eed57846a7486a9c87a095b5236957f7069ccc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273742672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfefc22388b8949ae9a0ebfa8e8255a7a16e978a1bf108cf9be61d9c15dd2a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:44:39 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 11 Aug 2023 01:44:39 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:44:40 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:45:31 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:45:33 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:45:33 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:45:33 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:45:33 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:45:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:45:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:45:39 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:45:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:45:40 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:45:41 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:45:41 GMT
USER 1001
# Fri, 11 Aug 2023 01:45:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804851dbab35ec8344fc34c03d1ed6514e1b03945b74193e356f87550a0f5013`  
		Last Modified: Fri, 11 Aug 2023 01:51:31 GMT  
		Size: 171.9 MB (171936546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7664eccc64979a403b0f2ffb852c00e5959dbcb02f071283b209aae88849efd8`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32785fd05d2c50a1da9ef78831c599820e5d6680389e068708d509fc88845a4b`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cbc7f9fed5d8353bd9bddf82c8ba30f1a1a7c38995d5d85ac42044195ed074`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856fb23a26853ef42fb2026eb3f8f12883e231d589b7df1cf971199103874ba`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4c78d76ceb7228bb9a35c33597bc17a356504fdf0295885dbbd88ae1994df`  
		Last Modified: Fri, 11 Aug 2023 01:51:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff920c65353a72b414fca77bbe736404060ceac1b85f4b4b0098adbc5a16a1e5`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af1523329e53a1f92910fb6f7044ede1f3859ecc668a9bbc38aa39ad01f6649`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:dfcff956c1450b989317e7f3c51a528688d012d9273d6a02f27945b9981befc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:8d16ac171b620f61410200cf4eed57846a7486a9c87a095b5236957f7069ccc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273742672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfefc22388b8949ae9a0ebfa8e8255a7a16e978a1bf108cf9be61d9c15dd2a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:44:39 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 11 Aug 2023 01:44:39 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:44:40 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:45:31 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:45:33 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:45:33 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:45:33 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:45:33 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:45:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:45:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:45:39 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:45:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:45:40 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:45:41 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:45:41 GMT
USER 1001
# Fri, 11 Aug 2023 01:45:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804851dbab35ec8344fc34c03d1ed6514e1b03945b74193e356f87550a0f5013`  
		Last Modified: Fri, 11 Aug 2023 01:51:31 GMT  
		Size: 171.9 MB (171936546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7664eccc64979a403b0f2ffb852c00e5959dbcb02f071283b209aae88849efd8`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32785fd05d2c50a1da9ef78831c599820e5d6680389e068708d509fc88845a4b`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cbc7f9fed5d8353bd9bddf82c8ba30f1a1a7c38995d5d85ac42044195ed074`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856fb23a26853ef42fb2026eb3f8f12883e231d589b7df1cf971199103874ba`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4c78d76ceb7228bb9a35c33597bc17a356504fdf0295885dbbd88ae1994df`  
		Last Modified: Fri, 11 Aug 2023 01:51:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff920c65353a72b414fca77bbe736404060ceac1b85f4b4b0098adbc5a16a1e5`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af1523329e53a1f92910fb6f7044ede1f3859ecc668a9bbc38aa39ad01f6649`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
