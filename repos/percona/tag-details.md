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
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
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
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.39`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.39` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.39-centos`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.39-centos` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.33-25`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.33-25` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.33-25-centos`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.33-25-centos` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
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
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.39`

```console
$ docker pull percona@sha256:022ac1e3826ea439f989c835da4f621a54d7a77cc49b656eef10cc65e2f3f743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.39` - linux; amd64

```console
$ docker pull percona@sha256:c83c778ff54c5d530d27e07d9f04b799fb9ec5a6eb1e9de6f463c5b05ff9551f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418369972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b0404d8440bce946c8c3ceb41f8d1a6976be42842a011e8f9fa9f60f1d5cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:44:58 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 22 Jul 2023 01:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 22 Jul 2023 01:45:34 GMT
ENV PS_VERSION=5.7.39-42.1
# Sat, 22 Jul 2023 01:45:34 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:45:34 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Sat, 22 Jul 2023 01:46:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 22 Jul 2023 01:46:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 22 Jul 2023 01:46:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 22 Jul 2023 01:46:13 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Sat, 22 Jul 2023 01:46:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:46:13 GMT
USER mysql
# Sat, 22 Jul 2023 01:46:13 GMT
EXPOSE 3306
# Sat, 22 Jul 2023 01:46:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d697f760dacb7f7054b3a15dc9e64227f6ece45855aa54a93e51aadfddfd18f`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1eb827dd8c9aaa1878d2a4eddebae645e1806016595dfd9e0b80d0fc2abe4`  
		Last Modified: Sat, 22 Jul 2023 01:51:37 GMT  
		Size: 191.9 MB (191894814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636bd663362195a51fd9e219283de62f67e12610965f8357bc885d206667621`  
		Last Modified: Sat, 22 Jul 2023 01:51:45 GMT  
		Size: 137.5 MB (137542479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de26af55c1e815a543d4099e2deccf67858ee1d43ab3d3b0253e16fe0a3aaa9`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7e8aebdff67446e73628fa353e97dfc80b80e0d6f806f8168e82ff04c9cd8`  
		Last Modified: Sat, 22 Jul 2023 01:51:27 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.33-25`

```console
$ docker pull percona@sha256:6f60b35e5f518e0dd46237895a4dba83b8e3e76328197299ea972600caf7d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.33-25` - linux; amd64

```console
$ docker pull percona@sha256:8babb7b44f39864e7fc11374d93d3f852d2d1ec9a15a6a0f1cda14b020958419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383335198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce2b3c131386b54b83e7022b5128dece4a3f50b6fe41733f00a72a98aa69f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jun 2023 00:23:56 GMT
ADD file:a5dc577a850ef41488490ddc01c977760aaa7fc688e77923c15be6c9f12674af in / 
# Fri, 23 Jun 2023 00:23:56 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 00:41:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 23 Jun 2023 00:41:13 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 23 Jun 2023 00:41:13 GMT
ENV OS_VER=el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 23 Jun 2023 00:41:13 GMT
ENV PS_REPO=testing
# Fri, 23 Jun 2023 00:41:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 23 Jun 2023 00:42:07 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 23 Jun 2023 00:42:11 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 23 Jun 2023 00:42:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2023 00:42:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 23 Jun 2023 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 00:42:12 GMT
USER mysql
# Fri, 23 Jun 2023 00:42:12 GMT
EXPOSE 3306 33060
# Fri, 23 Jun 2023 00:42:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd5367e01a11dce2026f7954fed19fca5829ed8a5816767ce069cda19e8b880e`  
		Last Modified: Fri, 23 Jun 2023 00:25:15 GMT  
		Size: 88.0 MB (87962811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce2f5c31c83f94f136286aa47a15096ef1fe91e17aa8a4565af115549f15f`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57914938b6feea2ca15088c32824fe36d315d524ba6143be76f4d1a1338b74a2`  
		Last Modified: Fri, 23 Jun 2023 00:42:58 GMT  
		Size: 7.3 MB (7326811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d313ab89a3ab23608351b5f778095610efdbc000dc174d4881221ce2ba4309`  
		Last Modified: Fri, 23 Jun 2023 00:43:37 GMT  
		Size: 288.0 MB (288039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e5e66ea115bc515f1cbadaf38bc07a1bfac33017e96ad729ea3443492fb2c`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0115118d13b5c42a3029767175c1727983b42050a09862aa94a51298d945e62`  
		Last Modified: Fri, 23 Jun 2023 00:42:57 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:6d037151ba2c77cccb9d4bc46b89bcba9c58e02dc4fc28dcbf5e30e7744bfa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:087d8663bdfe11637535d12b7e960409cabf248ed99a24f28dc251040a915f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219082302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4c5df10ff5dc98e5623c3fbfdbe9e23feb7519ad0a2a24bedb9eca7968dc16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 22 Jul 2023 01:49:53 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:50:44 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:50:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:50:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:50:45 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:50:45 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:50:48 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:50:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:50:51 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:50:51 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:50:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:50:51 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:50:51 GMT
USER 1001
# Sat, 22 Jul 2023 01:50:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e59d8262edc3761fc898e9536e1bfd4d42b54084ca172bbe7a069bcfba1038`  
		Last Modified: Sat, 22 Jul 2023 01:53:44 GMT  
		Size: 3.8 MB (3801613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdafea38407c8a9d31b4df88b7a4a835c3ff93c073cdfa0b6c0841f16c367da7`  
		Last Modified: Sat, 22 Jul 2023 01:53:58 GMT  
		Size: 117.3 MB (117266765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f243375913fb722f206536fe7d21f036323e3de7585dd16b36dfdf03c19249`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc426d1182cc48c6c89f5d43910971a3f6fcbb8b5ef6b8df1251a1c0974ebb6`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3c1f5a6509565113e9392906b87704e74702877ceffd9a84e9e1077dfcd20`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4f26de695f52cf4f4eebdd15fd211b107c5c0d2658b83b1123ab3fb55c177`  
		Last Modified: Sat, 22 Jul 2023 01:53:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4c6e7f357e0685b71f96235c37fba23de26f53af95f4ce2d5305987b312ce1`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b828ae934356e274e079c90de0639e81e129e0837564cbac8edd1325d6941e`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:6d037151ba2c77cccb9d4bc46b89bcba9c58e02dc4fc28dcbf5e30e7744bfa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:087d8663bdfe11637535d12b7e960409cabf248ed99a24f28dc251040a915f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219082302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4c5df10ff5dc98e5623c3fbfdbe9e23feb7519ad0a2a24bedb9eca7968dc16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 22 Jul 2023 01:49:53 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:50:44 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:50:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:50:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:50:45 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:50:45 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:50:48 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:50:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:50:51 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:50:51 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:50:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:50:51 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:50:51 GMT
USER 1001
# Sat, 22 Jul 2023 01:50:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e59d8262edc3761fc898e9536e1bfd4d42b54084ca172bbe7a069bcfba1038`  
		Last Modified: Sat, 22 Jul 2023 01:53:44 GMT  
		Size: 3.8 MB (3801613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdafea38407c8a9d31b4df88b7a4a835c3ff93c073cdfa0b6c0841f16c367da7`  
		Last Modified: Sat, 22 Jul 2023 01:53:58 GMT  
		Size: 117.3 MB (117266765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f243375913fb722f206536fe7d21f036323e3de7585dd16b36dfdf03c19249`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc426d1182cc48c6c89f5d43910971a3f6fcbb8b5ef6b8df1251a1c0974ebb6`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3c1f5a6509565113e9392906b87704e74702877ceffd9a84e9e1077dfcd20`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4f26de695f52cf4f4eebdd15fd211b107c5c0d2658b83b1123ab3fb55c177`  
		Last Modified: Sat, 22 Jul 2023 01:53:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4c6e7f357e0685b71f96235c37fba23de26f53af95f4ce2d5305987b312ce1`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b828ae934356e274e079c90de0639e81e129e0837564cbac8edd1325d6941e`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:ce9b4da67e41a942df161bfdea39727f996063a307ddde59129a1a91167be2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:b7916dd2b6e8464b9a18e349dbe9d904cebd6bac4c17f14b8562e53b46fab4cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237613434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b78758d1c0bb970d51df4954d754e2f3c683b22665fc89cb8be5d0c80d44ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 22 Jul 2023 01:48:43 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:32 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:49:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:49:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:49:34 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:49:34 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:49:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:49:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:49:39 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:49:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:49:40 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 22 Jul 2023 01:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:49:40 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:49:40 GMT
USER 1001
# Sat, 22 Jul 2023 01:49:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc79af77c7d33948209cb4ab3b7c748b48915e5e82605f46fdd97a7e7c1df3`  
		Last Modified: Sat, 22 Jul 2023 01:53:32 GMT  
		Size: 135.8 MB (135798244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a507dba314d7c69087bf0b3ee2474ffef7e5499b6cf2a5a235363b154bac26`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e2ebfbee8e0b99ef6552f2ba3bc1a49b1d0f74574b3017e7cbf18b377307a`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95390feb4e5ca96441e52c5692d764a473ca4c36264a9bfdd4a5a43695396c9`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ada12120e29efb25592448d1a953981c58c7e8bd80e12b8555076400848084`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf52c6c31b49cf96cd4e9c052d07320fb813d4f1823dc905c403838263347c4b`  
		Last Modified: Sat, 22 Jul 2023 01:53:14 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68627a4717e1892f28e31967dd09568e9857744cb956c2e96717190acb0581ae`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a58f08dfffc0689e3c9e4f91b911f776957437bdc4d2199a0d80deb29059ece`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:ce9b4da67e41a942df161bfdea39727f996063a307ddde59129a1a91167be2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:b7916dd2b6e8464b9a18e349dbe9d904cebd6bac4c17f14b8562e53b46fab4cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237613434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b78758d1c0bb970d51df4954d754e2f3c683b22665fc89cb8be5d0c80d44ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 22 Jul 2023 01:48:43 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:32 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:49:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:49:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:49:34 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:49:34 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:49:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:49:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:49:39 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:49:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:49:40 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 22 Jul 2023 01:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:49:40 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:49:40 GMT
USER 1001
# Sat, 22 Jul 2023 01:49:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc79af77c7d33948209cb4ab3b7c748b48915e5e82605f46fdd97a7e7c1df3`  
		Last Modified: Sat, 22 Jul 2023 01:53:32 GMT  
		Size: 135.8 MB (135798244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a507dba314d7c69087bf0b3ee2474ffef7e5499b6cf2a5a235363b154bac26`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e2ebfbee8e0b99ef6552f2ba3bc1a49b1d0f74574b3017e7cbf18b377307a`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95390feb4e5ca96441e52c5692d764a473ca4c36264a9bfdd4a5a43695396c9`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ada12120e29efb25592448d1a953981c58c7e8bd80e12b8555076400848084`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf52c6c31b49cf96cd4e9c052d07320fb813d4f1823dc905c403838263347c4b`  
		Last Modified: Sat, 22 Jul 2023 01:53:14 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68627a4717e1892f28e31967dd09568e9857744cb956c2e96717190acb0581ae`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a58f08dfffc0689e3c9e4f91b911f776957437bdc4d2199a0d80deb29059ece`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:382b30d8c925811eb4f77f9d504705d4d9af72983922a2d9ccd7bc2ea0eb1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:aa7e54a4b7e946ea50dc44cdbca34339572de5161556fdb841fd231204b19e6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250223819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f6b60f22d3c352c4bd3e7550f43bf07301e07c16e8b2312ada7a1062d6e715`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 22 Jul 2023 01:47:33 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:48:23 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:48:24 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:48:24 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:48:25 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:48:25 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:48:27 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:48:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:48:30 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:48:31 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:48:31 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:48:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:48:31 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:48:31 GMT
USER 1001
# Sat, 22 Jul 2023 01:48:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530c77d4061f301dc34466e1923c214a777e1bc493cc2425b2cc9155989b359`  
		Last Modified: Sat, 22 Jul 2023 01:53:02 GMT  
		Size: 148.4 MB (148408642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0785a0c71196b769fa2ba8f8c9751cf1db7396456fe22fe7b9980a8b765f6ba`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3921a48dd375b61e19241e9792d095a5595ac9a4a141161211b8158fc9f86fe1`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9943d42580bf59253114c86cf504850073eb84721926aa1f58fd200937f4409a`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ca833f799b9eb4728b8c7698afe74920c15d0078a8c7021b24d2f321b1afd0`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bfe35eef2a5b5649572e5da484c166e974ead34bdfb83c065677b636b5525b`  
		Last Modified: Sat, 22 Jul 2023 01:52:43 GMT  
		Size: 8.1 MB (8137883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c8da5f61229ba5b954d14e7dae0ac5008feb2639800e1bbf1198298cb638e8`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99922085625f2fb09526d7e5905cdff8c77138b9f50db9136a2c809e4d03f9`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:382b30d8c925811eb4f77f9d504705d4d9af72983922a2d9ccd7bc2ea0eb1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:aa7e54a4b7e946ea50dc44cdbca34339572de5161556fdb841fd231204b19e6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250223819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f6b60f22d3c352c4bd3e7550f43bf07301e07c16e8b2312ada7a1062d6e715`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 22 Jul 2023 01:47:33 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:48:23 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:48:24 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:48:24 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:48:25 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:48:25 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:48:27 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:48:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:48:30 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:48:31 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:48:31 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:48:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:48:31 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:48:31 GMT
USER 1001
# Sat, 22 Jul 2023 01:48:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530c77d4061f301dc34466e1923c214a777e1bc493cc2425b2cc9155989b359`  
		Last Modified: Sat, 22 Jul 2023 01:53:02 GMT  
		Size: 148.4 MB (148408642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0785a0c71196b769fa2ba8f8c9751cf1db7396456fe22fe7b9980a8b765f6ba`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3921a48dd375b61e19241e9792d095a5595ac9a4a141161211b8158fc9f86fe1`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9943d42580bf59253114c86cf504850073eb84721926aa1f58fd200937f4409a`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ca833f799b9eb4728b8c7698afe74920c15d0078a8c7021b24d2f321b1afd0`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bfe35eef2a5b5649572e5da484c166e974ead34bdfb83c065677b636b5525b`  
		Last Modified: Sat, 22 Jul 2023 01:52:43 GMT  
		Size: 8.1 MB (8137883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c8da5f61229ba5b954d14e7dae0ac5008feb2639800e1bbf1198298cb638e8`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99922085625f2fb09526d7e5905cdff8c77138b9f50db9136a2c809e4d03f9`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:9ac424c4a8111fed162c7d8c006b12d7af992d574c5909934991eb9f90c137d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:b73dad1b8266a63e028a19d67b10a7f35a032022e1cde5ce35d2f5322c33009c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273281720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3b143e96f4a2d4656ee8070cffdcaf2a593176f2ec5b94247777e4fdca1c1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 22 Jul 2023 01:46:26 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:47:19 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:47:20 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:47:20 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:47:21 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:47:21 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:47:24 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:47:27 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:47:28 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:47:28 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:47:28 GMT
USER 1001
# Sat, 22 Jul 2023 01:47:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204ac45a03315a5f6a8b29c06b73155c99ce39963cc0b373a2204ebf3b39a949`  
		Last Modified: Sat, 22 Jul 2023 01:52:33 GMT  
		Size: 171.5 MB (171466521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf54010b1edafbe136984c45019fd89c2e4b76e4ade03f7815711bbac9bdbd`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042513575f01729ea24f839a4f1d513648a9d25a33575f1c4908cc97b3889d65`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d9411ec8b7ce61275eb5fe1f03e9d6f749047513cb3aaa771c2abce89d0821`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb155650ddce25c425d293ced38bfbf03cb3a7b3cfe01162b23e10ffcb3a1b`  
		Last Modified: Sat, 22 Jul 2023 01:52:11 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd16c18633ef245ba79a9db2a6667e94351a8d3db11b3995819f61fe54b149b`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bce9efd7e0ed38913c714ed797d5a423ab4aa5358aaee5526e61de9c632e6d0`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0945b528b3fd8c59638a49e6b3b897e3cdf42fc6d914d3a7523921837696d73`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:9ac424c4a8111fed162c7d8c006b12d7af992d574c5909934991eb9f90c137d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:b73dad1b8266a63e028a19d67b10a7f35a032022e1cde5ce35d2f5322c33009c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273281720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3b143e96f4a2d4656ee8070cffdcaf2a593176f2ec5b94247777e4fdca1c1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 22 Jul 2023 01:46:26 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:47:19 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:47:20 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:47:20 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:47:21 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:47:21 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:47:24 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:47:27 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:47:28 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:47:28 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:47:28 GMT
USER 1001
# Sat, 22 Jul 2023 01:47:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204ac45a03315a5f6a8b29c06b73155c99ce39963cc0b373a2204ebf3b39a949`  
		Last Modified: Sat, 22 Jul 2023 01:52:33 GMT  
		Size: 171.5 MB (171466521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf54010b1edafbe136984c45019fd89c2e4b76e4ade03f7815711bbac9bdbd`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042513575f01729ea24f839a4f1d513648a9d25a33575f1c4908cc97b3889d65`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d9411ec8b7ce61275eb5fe1f03e9d6f749047513cb3aaa771c2abce89d0821`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb155650ddce25c425d293ced38bfbf03cb3a7b3cfe01162b23e10ffcb3a1b`  
		Last Modified: Sat, 22 Jul 2023 01:52:11 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd16c18633ef245ba79a9db2a6667e94351a8d3db11b3995819f61fe54b149b`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bce9efd7e0ed38913c714ed797d5a423ab4aa5358aaee5526e61de9c632e6d0`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0945b528b3fd8c59638a49e6b3b897e3cdf42fc6d914d3a7523921837696d73`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
