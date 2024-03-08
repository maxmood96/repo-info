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
-	[`percona:5.7.44`](#percona5744)
-	[`percona:5.7.44-centos`](#percona5744-centos)
-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.36-28`](#percona8036-28)
-	[`percona:8.0.36-28-centos`](#percona8036-28-centos)
-	[`percona:centos`](#perconacentos)
-	[`percona:ps-5`](#perconaps-5)
-	[`percona:ps-5.6`](#perconaps-56)
-	[`percona:ps-5.6.51-2`](#perconaps-5651-2)
-	[`percona:ps-5.7`](#perconaps-57)
-	[`percona:ps-5.7.44`](#perconaps-5744)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.36-28`](#perconaps-8036-28)
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
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
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
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28-centos`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28-centos` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
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
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.36-28`

```console
$ docker pull percona@sha256:8b1565301ff5deeb0c7ec8e205ba634fe7bc5732a7bd51d18770774cc519268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:7ec83880489c6f5255b55ee213cce27e92516034c76cb1e335dad553f79089bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a86d4135d1f20f7279e48fd1644b7aa6d215734cd8c4f1be4ccdb888adf3f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:20:49 GMT
ADD file:c57b89b3a2cb23d81840b83c9df4abe2434b6de85cd143c0711377e360761412 in / 
# Fri, 08 Mar 2024 19:20:50 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:38:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:38:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_VERSION=8.0.36-28.1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Fri, 08 Mar 2024 19:38:41 GMT
ENV OS_VER=el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Fri, 08 Mar 2024 19:38:41 GMT
ENV PS_REPO=release
# Fri, 08 Mar 2024 19:38:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:38:42 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:38:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:38:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 08 Mar 2024 19:39:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:39:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 08 Mar 2024 19:39:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:39:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:39:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 Mar 2024 19:39:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:39:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:39:56 GMT
USER mysql
# Fri, 08 Mar 2024 19:39:56 GMT
EXPOSE 3306 33060
# Fri, 08 Mar 2024 19:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8194e57f93aec018b1114d96923bcc8b57abeca7e1bde58ff255a66966de3464`  
		Last Modified: Fri, 08 Mar 2024 19:22:20 GMT  
		Size: 95.2 MB (95169007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3a8b6851a683db5a1c66cbb875734f45145a0eb8430ba256849545948e8af`  
		Last Modified: Fri, 08 Mar 2024 19:46:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458af3fb77c78c0082f8398acaff9983270a2116a5a65bfb6eb09b3942d061`  
		Last Modified: Fri, 08 Mar 2024 19:46:57 GMT  
		Size: 7.3 MB (7319522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d42e3e00c62fbdb3ef5f538f2fcf6d1401d0d369241dba8aa696e73bd3ad`  
		Last Modified: Fri, 08 Mar 2024 19:47:38 GMT  
		Size: 296.0 MB (296031502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c09a0c26f9a77671ce2fef85a59f248716f870a3b9e9d2cb00467abad3329`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ee211fd29c24ba4f92abf855c385973f09c5b966a6e20e1a13387b88764b2`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2a6f7b742a29f7b1b9e953da7a18ec0063938a43822ff68ecd7998de34385`  
		Last Modified: Fri, 08 Mar 2024 19:46:56 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:4b02ab29c024a8a3de8dbda2aaa02be459f7bf137975bfb73f74a4d044cf330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:b49cac9506892b5853a80e96479b1d2c2a87f6a68b171c73abf2e42f7c8310bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231963063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749956f05d28366b18c3a78f0db22a8d79d91accc59b7aeecf45ee5b277b2778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 08 Mar 2024 19:45:30 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:46:24 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:46:25 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:46:25 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:46:26 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:46:26 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:46:29 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:46:31 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:46:31 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:46:31 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:46:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:46:32 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:46:32 GMT
USER 1001
# Fri, 08 Mar 2024 19:46:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d30b856bbfc5b0d02fa88a7c4f2d29c4bef830bff12f467ece789abfdef7c4a`  
		Last Modified: Fri, 08 Mar 2024 19:50:16 GMT  
		Size: 4.3 MB (4304227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608d01d2a1faaf5a21a940e534c16066095b0d8322f30e7c077357607ceb233`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 117.8 MB (117771915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034ba415818b29f68a1b3f05ec21c7800f09b15e7297128692f1c5937d4469`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41cdbae717278a6b00499d4d5094d0651b94f56bcc5f4b34e33193371b24297`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7bb8c77c2027e35e6f8cef6991baaf4527b27db92bd246a57b222a7b01c465`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ebb89f9b0b8218a3ab5fa29c08d012cab229d4173f4850869f5a532f662626`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86f8d408851cc2a7df3c2a0aee79d843a7742d151e91cdf203892739ba05e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 8.2 MB (8151464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa78d4184def64aa834478252e8a3b11c6774552d09748aadadbbfc0c73a0c7d`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:4b02ab29c024a8a3de8dbda2aaa02be459f7bf137975bfb73f74a4d044cf330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:b49cac9506892b5853a80e96479b1d2c2a87f6a68b171c73abf2e42f7c8310bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231963063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749956f05d28366b18c3a78f0db22a8d79d91accc59b7aeecf45ee5b277b2778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 08 Mar 2024 19:45:30 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:46:24 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:46:25 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:46:25 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:46:26 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:46:26 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:46:29 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:46:31 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:46:31 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:46:31 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:46:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:46:32 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:46:32 GMT
USER 1001
# Fri, 08 Mar 2024 19:46:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d30b856bbfc5b0d02fa88a7c4f2d29c4bef830bff12f467ece789abfdef7c4a`  
		Last Modified: Fri, 08 Mar 2024 19:50:16 GMT  
		Size: 4.3 MB (4304227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608d01d2a1faaf5a21a940e534c16066095b0d8322f30e7c077357607ceb233`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 117.8 MB (117771915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034ba415818b29f68a1b3f05ec21c7800f09b15e7297128692f1c5937d4469`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41cdbae717278a6b00499d4d5094d0651b94f56bcc5f4b34e33193371b24297`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7bb8c77c2027e35e6f8cef6991baaf4527b27db92bd246a57b222a7b01c465`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ebb89f9b0b8218a3ab5fa29c08d012cab229d4173f4850869f5a532f662626`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86f8d408851cc2a7df3c2a0aee79d843a7742d151e91cdf203892739ba05e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 8.2 MB (8151464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa78d4184def64aa834478252e8a3b11c6774552d09748aadadbbfc0c73a0c7d`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:de87f299e14abdafef2687c28c55cf8867f1add009ed24e215b668ba85ab2b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:3895740832ccd6ba8c74fd4c9dc833516181d3acada06a0210489ba2f75bd630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250498367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629065e2d8b415544c10136e9e392ff3f0c61569f1dae6061360d5859b65d49f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:44:20 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 08 Mar 2024 19:44:20 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:44:20 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 08 Mar 2024 19:44:20 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:44:20 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:45:14 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:45:15 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:45:15 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:45:15 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:45:15 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:45:19 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:45:21 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:45:21 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:45:22 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:45:22 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 08 Mar 2024 19:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:45:22 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:45:22 GMT
USER 1001
# Fri, 08 Mar 2024 19:45:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b49aa1f002a8ef6f67744a6a0bc0c84170f055d3c765f64651a1aa6b206bf`  
		Last Modified: Fri, 08 Mar 2024 19:50:05 GMT  
		Size: 136.3 MB (136307625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8465e530d231ed0d005ce7c8e809e72eba0ec04d4d12de0c5d9c3af05381ff71`  
		Last Modified: Fri, 08 Mar 2024 19:49:46 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c91f7be4cfbf55dec60ca7445ed895ae9c0a8639d204e02a72a2550060315d`  
		Last Modified: Fri, 08 Mar 2024 19:49:45 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ffb16a900889b3fb3a0b81a35ee483ff5a95a58c851c496e5dee9bacf967c7`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1acc9ee71abd6b5e12cca17c9ac2cd4ce9c9a0f914e6ebb7a2a25f73c29ad9`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662f737e2a08c3247e4729c2a1362b03e64beab53d3b33d32c822bdb26f2a736`  
		Last Modified: Fri, 08 Mar 2024 19:49:45 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c9e5c6369e2af01a34e607d33f595d8def9d854cc5078bd96f27253415d66c`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d45691a8beb0be1ed661d94d799c805bcf38285828c0e42f0dd11e4a7593143`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:de87f299e14abdafef2687c28c55cf8867f1add009ed24e215b668ba85ab2b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:3895740832ccd6ba8c74fd4c9dc833516181d3acada06a0210489ba2f75bd630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250498367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629065e2d8b415544c10136e9e392ff3f0c61569f1dae6061360d5859b65d49f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:44:20 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 08 Mar 2024 19:44:20 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:44:20 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 08 Mar 2024 19:44:20 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:44:20 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:45:14 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:45:15 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:45:15 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:45:15 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:45:15 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:45:19 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:45:21 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:45:21 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:45:22 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:45:22 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 08 Mar 2024 19:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:45:22 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:45:22 GMT
USER 1001
# Fri, 08 Mar 2024 19:45:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b49aa1f002a8ef6f67744a6a0bc0c84170f055d3c765f64651a1aa6b206bf`  
		Last Modified: Fri, 08 Mar 2024 19:50:05 GMT  
		Size: 136.3 MB (136307625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8465e530d231ed0d005ce7c8e809e72eba0ec04d4d12de0c5d9c3af05381ff71`  
		Last Modified: Fri, 08 Mar 2024 19:49:46 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c91f7be4cfbf55dec60ca7445ed895ae9c0a8639d204e02a72a2550060315d`  
		Last Modified: Fri, 08 Mar 2024 19:49:45 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ffb16a900889b3fb3a0b81a35ee483ff5a95a58c851c496e5dee9bacf967c7`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1acc9ee71abd6b5e12cca17c9ac2cd4ce9c9a0f914e6ebb7a2a25f73c29ad9`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662f737e2a08c3247e4729c2a1362b03e64beab53d3b33d32c822bdb26f2a736`  
		Last Modified: Fri, 08 Mar 2024 19:49:45 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c9e5c6369e2af01a34e607d33f595d8def9d854cc5078bd96f27253415d66c`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d45691a8beb0be1ed661d94d799c805bcf38285828c0e42f0dd11e4a7593143`  
		Last Modified: Fri, 08 Mar 2024 19:49:44 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:ee5561ecc7ad795406d6ac7a116920fbf6ab61c9dd29dc3e53b05e37ed36fc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:2ec031cd1b4589c3a0287fc0d9d97a6486ffd133fe27006b7036575269a0e828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263093105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8222ad5d77178c7dbe7fd22aac53086d0bd6dc1fccd111b57acdbd41117af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 08 Mar 2024 19:43:10 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:44:04 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:44:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:44:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:44:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:44:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:44:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:44:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:44:11 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:44:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:44:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:44:12 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:44:12 GMT
USER 1001
# Fri, 08 Mar 2024 19:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d9b581cbd02d1ec08e8ac9cf8fc97109d0916cd7065197385a0bf66803f7a5`  
		Last Modified: Fri, 08 Mar 2024 19:49:36 GMT  
		Size: 148.9 MB (148902362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c204532e44c8f3ab43d178a889534a5c210f0d85510619b86cf277b657abf`  
		Last Modified: Fri, 08 Mar 2024 19:49:18 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bf7efcec6bb93fa2121f9de2fd00b6a7124d7dc2df17cc797b7507442b8ae2`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17277d42ba1e087b1cf7c6a03c3c22bdc5bac483b3289b90e45efc54159e7112`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b52f897ee0f00f4da3b38fb122b63028e1b42eb6948d0a66a95b9e537cff61`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1677cb1b77e96204568415dc760219aa5636bc2e6b07903a930524653b68deed`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef777dcb174af13243d2a6818992d5c59dabe5e02b362effbebbfdbd7bedb2`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b5624348b624bbb01acd4d60187256e5a904221e953f41e51edeab88c80810`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:ee5561ecc7ad795406d6ac7a116920fbf6ab61c9dd29dc3e53b05e37ed36fc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:2ec031cd1b4589c3a0287fc0d9d97a6486ffd133fe27006b7036575269a0e828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263093105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8222ad5d77178c7dbe7fd22aac53086d0bd6dc1fccd111b57acdbd41117af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 08 Mar 2024 19:43:10 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:44:04 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:44:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:44:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:44:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:44:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:44:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:44:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:44:11 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:44:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:44:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:44:12 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:44:12 GMT
USER 1001
# Fri, 08 Mar 2024 19:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d9b581cbd02d1ec08e8ac9cf8fc97109d0916cd7065197385a0bf66803f7a5`  
		Last Modified: Fri, 08 Mar 2024 19:49:36 GMT  
		Size: 148.9 MB (148902362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c204532e44c8f3ab43d178a889534a5c210f0d85510619b86cf277b657abf`  
		Last Modified: Fri, 08 Mar 2024 19:49:18 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bf7efcec6bb93fa2121f9de2fd00b6a7124d7dc2df17cc797b7507442b8ae2`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17277d42ba1e087b1cf7c6a03c3c22bdc5bac483b3289b90e45efc54159e7112`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b52f897ee0f00f4da3b38fb122b63028e1b42eb6948d0a66a95b9e537cff61`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1677cb1b77e96204568415dc760219aa5636bc2e6b07903a930524653b68deed`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef777dcb174af13243d2a6818992d5c59dabe5e02b362effbebbfdbd7bedb2`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b5624348b624bbb01acd4d60187256e5a904221e953f41e51edeab88c80810`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:e1f543ecab041850ce6abebaef13ee5e54b3b493cb11a0abddedab055897525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:787b3c63909d12c498a94d41e1d92cedd8a68bbb2d2ecce509d66c52de71a9ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286571607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392cdbe58c4136a20fdaa92f39d34b06487b62e4848c4a27b63c67a16f566c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 08 Mar 2024 19:41:49 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:42:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:42:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:42:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:42:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:42:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:42:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:42:55 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:42:55 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:42:56 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:42:56 GMT
USER 1001
# Fri, 08 Mar 2024 19:42:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74645974e5ba1cfc0eed468e337297d603c1a5a6eec3aa16d2fec89c65de9a9f`  
		Last Modified: Fri, 08 Mar 2024 19:49:07 GMT  
		Size: 172.4 MB (172380843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf08b3296571a78e7818cef8db205b81c9cfe8f98765170eed15f0a44142815`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd597b85c2b86d74fb78b9dbfa8dd68fcf69623e35899900a04a3a87819988`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda329fea3176232df37cba69c0ea5c6a4b224c9b5ca1393a159959851287ad8`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd31ae03eff8443ce798c7eac79ca7cda175706be5dbe96d7e5c265e4210542a`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69235949454acb09846f32770926bbcc7c4d4afbe53e45ae18656a4cb66d34`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab93e7a6b7d34b1450edb654540ee4b9645ee18e8a7da88f8c344e6ec677ea95`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39a6acf07b17bdb8963c98ae72a4a70000c886505ad3a8d63f96de53f3563bf`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:e1f543ecab041850ce6abebaef13ee5e54b3b493cb11a0abddedab055897525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:787b3c63909d12c498a94d41e1d92cedd8a68bbb2d2ecce509d66c52de71a9ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286571607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392cdbe58c4136a20fdaa92f39d34b06487b62e4848c4a27b63c67a16f566c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 08 Mar 2024 19:41:49 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:42:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:42:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:42:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:42:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:42:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:42:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:42:55 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:42:55 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:42:56 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:42:56 GMT
USER 1001
# Fri, 08 Mar 2024 19:42:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74645974e5ba1cfc0eed468e337297d603c1a5a6eec3aa16d2fec89c65de9a9f`  
		Last Modified: Fri, 08 Mar 2024 19:49:07 GMT  
		Size: 172.4 MB (172380843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf08b3296571a78e7818cef8db205b81c9cfe8f98765170eed15f0a44142815`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd597b85c2b86d74fb78b9dbfa8dd68fcf69623e35899900a04a3a87819988`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda329fea3176232df37cba69c0ea5c6a4b224c9b5ca1393a159959851287ad8`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd31ae03eff8443ce798c7eac79ca7cda175706be5dbe96d7e5c265e4210542a`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69235949454acb09846f32770926bbcc7c4d4afbe53e45ae18656a4cb66d34`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab93e7a6b7d34b1450edb654540ee4b9645ee18e8a7da88f8c344e6ec677ea95`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39a6acf07b17bdb8963c98ae72a4a70000c886505ad3a8d63f96de53f3563bf`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
