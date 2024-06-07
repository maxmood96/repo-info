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
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
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
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28-centos`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28-centos` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
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
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.36-28`

```console
$ docker pull percona@sha256:492cb7e0a1224e7a81230b8228133da9a2c593b74a2dfb274722a9cec2c883d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:ab72d1627bd39322d8edd91fd32d6044ed3f659f9aa1f5684b3bd9875686bfac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398821342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4d5ebef525842bc60e46666d9ecdd7980dd4314af62d41eb3b914caf4052d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:48 GMT
ADD file:10cd00b53a09be8fe6fb65bb981249a702bd2a67fcde6d3e8008a7e7645f3a7f in / 
# Sat, 01 Jun 2024 00:47:49 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:37:11 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:37:11 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV OS_VER=el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_REPO=release
# Sat, 01 Jun 2024 01:37:12 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:37:12 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:37:12 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:37:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 01 Jun 2024 01:38:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:38:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 01 Jun 2024 01:38:30 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:38:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:38:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 01 Jun 2024 01:38:31 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:38:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:38:32 GMT
USER mysql
# Sat, 01 Jun 2024 01:38:32 GMT
EXPOSE 3306 33060
# Sat, 01 Jun 2024 01:38:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:94fc9838e1d564bd9488e2890b503cade665872049b28c58bcc89501ac7f837f`  
		Last Modified: Sat, 01 Jun 2024 00:49:46 GMT  
		Size: 95.5 MB (95450234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393045b94b9c573a272f31dde4b260cc2684f8a6fdf7210ed776352639a8aab`  
		Last Modified: Sat, 01 Jun 2024 01:45:58 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658058a3d75f8b98b606c8078c5ab526c0fee4895f6603ad54a4833cbf0408c2`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 7.3 MB (7322013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b915d239d3ebe42328198df7a53c3221515aa265410529dae92f0d809dc5c8`  
		Last Modified: Sat, 01 Jun 2024 01:46:37 GMT  
		Size: 296.0 MB (296039051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc63bca08a02a16cb5423eea17c054a53df915eff98696b920f6b1acbe45d7`  
		Last Modified: Sat, 01 Jun 2024 01:45:56 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e443731296c584a8e7fc7a03dc5b6f78b7dcd5c667643863a55ac1b8a255671`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a888ba58c578625e4ad265c27261fc75ed52a239178014c127296c7207ff6d`  
		Last Modified: Sat, 01 Jun 2024 01:45:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:bff1f77c4e9286adb71389cf9dde8bc67ea1cfe17084d4d8a58773c629636191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:5bd6f16d9a672d699ac23241ed39a86af76b5a60e45c458af3b62c81ecf9cb0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231904978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f463ddcd893b5119fa877b96112343c0e757c4451e709cc64be1269342190ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 05:03:39 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 07 Jun 2024 05:03:39 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:03:40 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 07 Jun 2024 05:03:40 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:03:40 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:03:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:04:37 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:04:39 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:04:39 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:04:39 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:04:39 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:04:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:04:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:04:45 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:04:45 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:04:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:04:45 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:04:45 GMT
USER 1001
# Fri, 07 Jun 2024 05:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f89364601e8310f471e70069c70fcf2a383fd8deada96d759cee10de8a324f`  
		Last Modified: Fri, 07 Jun 2024 05:07:22 GMT  
		Size: 4.3 MB (4311014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2880f32e2d459bd2304366588320ee23b9fce909bb351749317c61dfe83d3`  
		Last Modified: Fri, 07 Jun 2024 05:07:36 GMT  
		Size: 117.8 MB (117791993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcc8d6a7c76171936f28ff975eceeac5284ef1de1661f06549413eac69db1bd`  
		Last Modified: Fri, 07 Jun 2024 05:07:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d06bd40fbed38ab9ee21ac39c0f798ce47f4b01d84641853ba99ec5ab4c8c21`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4c3a4e7879c2170d494fc61e9d5f193371afe2d68f67ce2fad75376d0f76a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd401d021d54e84c5d397f7a3543e0627c185558af448162c3298501ad6e669a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d125cbfc50d9971044f894c2bd6859e46f6cb614826deef6bd30cd2717262f1`  
		Last Modified: Fri, 07 Jun 2024 05:07:21 GMT  
		Size: 8.2 MB (8151447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a225e3d148540a92b00856077a6f47647104c7b0f088f3b27c3435f5118fb7a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:bff1f77c4e9286adb71389cf9dde8bc67ea1cfe17084d4d8a58773c629636191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:5bd6f16d9a672d699ac23241ed39a86af76b5a60e45c458af3b62c81ecf9cb0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231904978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f463ddcd893b5119fa877b96112343c0e757c4451e709cc64be1269342190ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 05:03:39 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 07 Jun 2024 05:03:39 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:03:40 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 07 Jun 2024 05:03:40 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:03:40 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:03:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:04:37 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:04:39 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:04:39 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:04:39 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:04:39 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:04:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:04:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:04:45 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:04:45 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:04:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:04:45 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:04:45 GMT
USER 1001
# Fri, 07 Jun 2024 05:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f89364601e8310f471e70069c70fcf2a383fd8deada96d759cee10de8a324f`  
		Last Modified: Fri, 07 Jun 2024 05:07:22 GMT  
		Size: 4.3 MB (4311014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2880f32e2d459bd2304366588320ee23b9fce909bb351749317c61dfe83d3`  
		Last Modified: Fri, 07 Jun 2024 05:07:36 GMT  
		Size: 117.8 MB (117791993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcc8d6a7c76171936f28ff975eceeac5284ef1de1661f06549413eac69db1bd`  
		Last Modified: Fri, 07 Jun 2024 05:07:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d06bd40fbed38ab9ee21ac39c0f798ce47f4b01d84641853ba99ec5ab4c8c21`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4c3a4e7879c2170d494fc61e9d5f193371afe2d68f67ce2fad75376d0f76a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd401d021d54e84c5d397f7a3543e0627c185558af448162c3298501ad6e669a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d125cbfc50d9971044f894c2bd6859e46f6cb614826deef6bd30cd2717262f1`  
		Last Modified: Fri, 07 Jun 2024 05:07:21 GMT  
		Size: 8.2 MB (8151447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a225e3d148540a92b00856077a6f47647104c7b0f088f3b27c3435f5118fb7a`  
		Last Modified: Fri, 07 Jun 2024 05:07:20 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:813c5a609ea503d65e14ba27ac3d6dfbc4cc1835d67de0b05e4b8d220763f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:9374786873ea0274db5a9838718bc6eff49b0f3b18a21481f406870228a2e53b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250413579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f79c3cc3d60adfb87f292e8387026ddae9c6c040776a6fbcca800b1183fbbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:02:29 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 07 Jun 2024 05:02:29 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:02:29 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 07 Jun 2024 05:02:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:02:30 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:03:26 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:03:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:03:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:03:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:03:28 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:03:31 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:03:34 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:03:34 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:03:35 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:03:35 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 07 Jun 2024 05:03:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:03:35 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:03:35 GMT
USER 1001
# Fri, 07 Jun 2024 05:03:35 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa590c1f0e690fac3e3220f855c77219b3cfdfe9cdcea1b1915b3b2364da07c7`  
		Last Modified: Fri, 07 Jun 2024 05:07:11 GMT  
		Size: 136.3 MB (136300866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671b10297711d10fad20bf9963c4cb7c06f529b7e26b7876e7e11f116d72fe14`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82afa0dcd4a3201785d300baa5519ad5d8ef4a5c0abcd56380a8efae3ed0e8c1`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4865702b602a42b7acb97031dccc42a14fe2fcedcc9bb6f6dd88a106cdeda11`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f105508597fcace3d9b7c539f95490a9df789fe1a4456baaa0cda8f93161dac7`  
		Last Modified: Fri, 07 Jun 2024 05:06:53 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68e29c121b581eb36e7a91995897d11eb47b0f5190d34f43960eab79b5a7a33`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f5fa3d33168c0001cbf61bf5998b683238b8bf7b48ca42d30c56687d7be33b`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a94fde5d2656b48c73c984ed9f3d344c3eb8be4461518996567b814c0b32d1`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:813c5a609ea503d65e14ba27ac3d6dfbc4cc1835d67de0b05e4b8d220763f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:9374786873ea0274db5a9838718bc6eff49b0f3b18a21481f406870228a2e53b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250413579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f79c3cc3d60adfb87f292e8387026ddae9c6c040776a6fbcca800b1183fbbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:02:29 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 07 Jun 2024 05:02:29 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:02:29 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 07 Jun 2024 05:02:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:02:30 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:03:26 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:03:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:03:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:03:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:03:28 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:03:31 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:03:34 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:03:34 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:03:35 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:03:35 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 07 Jun 2024 05:03:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:03:35 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:03:35 GMT
USER 1001
# Fri, 07 Jun 2024 05:03:35 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa590c1f0e690fac3e3220f855c77219b3cfdfe9cdcea1b1915b3b2364da07c7`  
		Last Modified: Fri, 07 Jun 2024 05:07:11 GMT  
		Size: 136.3 MB (136300866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671b10297711d10fad20bf9963c4cb7c06f529b7e26b7876e7e11f116d72fe14`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82afa0dcd4a3201785d300baa5519ad5d8ef4a5c0abcd56380a8efae3ed0e8c1`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4865702b602a42b7acb97031dccc42a14fe2fcedcc9bb6f6dd88a106cdeda11`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f105508597fcace3d9b7c539f95490a9df789fe1a4456baaa0cda8f93161dac7`  
		Last Modified: Fri, 07 Jun 2024 05:06:53 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68e29c121b581eb36e7a91995897d11eb47b0f5190d34f43960eab79b5a7a33`  
		Last Modified: Fri, 07 Jun 2024 05:06:54 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f5fa3d33168c0001cbf61bf5998b683238b8bf7b48ca42d30c56687d7be33b`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a94fde5d2656b48c73c984ed9f3d344c3eb8be4461518996567b814c0b32d1`  
		Last Modified: Fri, 07 Jun 2024 05:06:52 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:32c2cd66a3743c33db26125d47c9e343fb2301c8f42d5c9a247217f68fd28e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:f6d421f1e62bcb7b15ff1a4ac044f19756fea5f259b4d9082106a2ec17fed433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263022990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd54b00f6feaacd88fd7d197c07e51a2e04196a6491d79bf60953155b1810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:01:05 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 07 Jun 2024 05:01:05 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:01:05 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 07 Jun 2024 05:01:06 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:01:06 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:02:03 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:02:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:02:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:02:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:02:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:02:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:02:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:02:12 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:02:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:02:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:02:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:02:13 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:02:13 GMT
USER 1001
# Fri, 07 Jun 2024 05:02:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b859ddc030918c186ce06234efab6b6630c7694c8f1100867179eb20e7a63`  
		Last Modified: Fri, 07 Jun 2024 05:06:44 GMT  
		Size: 148.9 MB (148910273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e15d503e757081627b62b901873ff8882c0da835e7a7c98b88806e4520c296f`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d622a0bbdc622660b5f402106fec3c78eeee9dad098eb92b5d544f4569a3eaf8`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b31ac65a1d7a4a5f18e1679c049a4c51a87afc9af8a8a0eb38ae693e8942b0`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c0cb683b71415383cf6d56a210138dd08567939687b3a1cbf2ac3d3286f3`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fde1ee5ef5c08d6ea52b7654906334c43084fc7e0a9e11a04f9c66005b69545`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d064f6bd6355ae0d3af1cd92e5f4eba3bd0234a187a008e81bc2a4fd00d73c`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b46104c08228b516c7061b1368156309d85e3c273f6d9c4bb65f1a608f5290`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:32c2cd66a3743c33db26125d47c9e343fb2301c8f42d5c9a247217f68fd28e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:f6d421f1e62bcb7b15ff1a4ac044f19756fea5f259b4d9082106a2ec17fed433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263022990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd54b00f6feaacd88fd7d197c07e51a2e04196a6491d79bf60953155b1810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:01:05 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 07 Jun 2024 05:01:05 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:01:05 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 07 Jun 2024 05:01:06 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:01:06 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:02:03 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:02:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:02:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:02:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:02:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:02:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:02:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:02:12 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:02:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:02:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:02:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:02:13 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:02:13 GMT
USER 1001
# Fri, 07 Jun 2024 05:02:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b859ddc030918c186ce06234efab6b6630c7694c8f1100867179eb20e7a63`  
		Last Modified: Fri, 07 Jun 2024 05:06:44 GMT  
		Size: 148.9 MB (148910273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e15d503e757081627b62b901873ff8882c0da835e7a7c98b88806e4520c296f`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d622a0bbdc622660b5f402106fec3c78eeee9dad098eb92b5d544f4569a3eaf8`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b31ac65a1d7a4a5f18e1679c049a4c51a87afc9af8a8a0eb38ae693e8942b0`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c0cb683b71415383cf6d56a210138dd08567939687b3a1cbf2ac3d3286f3`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fde1ee5ef5c08d6ea52b7654906334c43084fc7e0a9e11a04f9c66005b69545`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d064f6bd6355ae0d3af1cd92e5f4eba3bd0234a187a008e81bc2a4fd00d73c`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b46104c08228b516c7061b1368156309d85e3c273f6d9c4bb65f1a608f5290`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:cc40737a9808ebc2dea3afb14ef06e6326c1fc9e36998fb7a97ca52492d13e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:212483f40376cf40de2632536ad1da071402ccac08db1ba5b70510c3b7e24df0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286535501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41264cea5dbc4e254ab5c448c34cda4855a54eb9ed777952ef520a7946cc7814`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 04:59:44 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 07 Jun 2024 04:59:44 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 04:59:45 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:00:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:00:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:00:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:00:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:00:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:00:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:00:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:00:55 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:00:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:00:56 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:00:56 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:00:56 GMT
USER 1001
# Fri, 07 Jun 2024 05:00:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9374102091b6de34f2ddfa589353b80ce2b2b880945837b04396d9be376b81f`  
		Last Modified: Fri, 07 Jun 2024 05:06:16 GMT  
		Size: 172.4 MB (172422786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4371d297efd24129c7be6e948344dff64a77e724cc4a66be262ecf219063c973`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d326c23dda258451a6d54935a883682971c745c8506363962cbf603bc227d785`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138dd2ee986baf9caabd344fcca10e3dbb7b0bdba5fca1a7ad771e7c86830c02`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56aa9e0a0a4508d8416e1a4d7aca5984a0b6f7acb4945da297e7ec35b98f27`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa813a9c3fe54bfc09094980b149818db9497eb51ed142df215367ac930dca3d`  
		Last Modified: Fri, 07 Jun 2024 05:05:55 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b84982c5e87b249d4b86fb989fc820edc15186d6b43e98c9c55e0187a4f28e1`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846edf16ad892df4e95b54ed9f29986629d635a2b46e22d1e0e6cc714f9e503c`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:cc40737a9808ebc2dea3afb14ef06e6326c1fc9e36998fb7a97ca52492d13e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:212483f40376cf40de2632536ad1da071402ccac08db1ba5b70510c3b7e24df0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286535501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41264cea5dbc4e254ab5c448c34cda4855a54eb9ed777952ef520a7946cc7814`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 04:59:44 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 07 Jun 2024 04:59:44 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 04:59:45 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:00:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:00:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:00:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:00:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:00:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:00:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:00:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:00:55 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:00:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:00:56 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:00:56 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:00:56 GMT
USER 1001
# Fri, 07 Jun 2024 05:00:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9374102091b6de34f2ddfa589353b80ce2b2b880945837b04396d9be376b81f`  
		Last Modified: Fri, 07 Jun 2024 05:06:16 GMT  
		Size: 172.4 MB (172422786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4371d297efd24129c7be6e948344dff64a77e724cc4a66be262ecf219063c973`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d326c23dda258451a6d54935a883682971c745c8506363962cbf603bc227d785`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138dd2ee986baf9caabd344fcca10e3dbb7b0bdba5fca1a7ad771e7c86830c02`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56aa9e0a0a4508d8416e1a4d7aca5984a0b6f7acb4945da297e7ec35b98f27`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa813a9c3fe54bfc09094980b149818db9497eb51ed142df215367ac930dca3d`  
		Last Modified: Fri, 07 Jun 2024 05:05:55 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b84982c5e87b249d4b86fb989fc820edc15186d6b43e98c9c55e0187a4f28e1`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846edf16ad892df4e95b54ed9f29986629d635a2b46e22d1e0e6cc714f9e503c`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
