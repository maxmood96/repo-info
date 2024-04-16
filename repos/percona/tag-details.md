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
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
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
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28-centos`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28-centos` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
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
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.36-28`

```console
$ docker pull percona@sha256:ca7f07ef67758e71420d5f5120d47ee8314b422e2ca13786ef589d58ff0ce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:4cc681a00e0c3fd5cfc41f7c20e9bc06cf39cb5cd2abe62e2327f48a0c77ff3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9bca2ccac5f9ebe5654b14f6f1d7adfd9423159fc8f65a63dcaa742476627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 29 Mar 2024 23:51:15 GMT
ADD file:62a6ccde6b31dc5c71f53fdf63e55acdf9bf5e1c1a03b57f84f34712a10ad212 in / 
# Fri, 29 Mar 2024 23:51:16 GMT
CMD ["/bin/bash"]
# Sat, 30 Mar 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 30 Mar 2024 00:07:57 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_VERSION=8.0.36-28.1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV OS_VER=el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_REPO=release
# Sat, 30 Mar 2024 00:07:57 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 30 Mar 2024 00:07:57 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 30 Mar 2024 00:07:58 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 30 Mar 2024 00:08:00 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Sat, 30 Mar 2024 00:09:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 30 Mar 2024 00:09:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Sat, 30 Mar 2024 00:09:15 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 30 Mar 2024 00:09:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 30 Mar 2024 00:09:16 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Sat, 30 Mar 2024 00:09:16 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Sat, 30 Mar 2024 00:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Mar 2024 00:09:16 GMT
USER mysql
# Sat, 30 Mar 2024 00:09:16 GMT
EXPOSE 3306 33060
# Sat, 30 Mar 2024 00:09:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe9c990952a7c7726d2172b9514fd752a082a6239c3cc7dc558d0ca4afa78868`  
		Last Modified: Fri, 29 Mar 2024 23:52:26 GMT  
		Size: 95.2 MB (95168175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97f8840f2f12d6ba292603c7400b0f0ed0253d2b065b3a7fff0e46332b2800`  
		Last Modified: Sat, 30 Mar 2024 00:09:53 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99423855e8b7649868adee546c5d236f43ceedd6c20bb802574669fe6978e1e9`  
		Last Modified: Sat, 30 Mar 2024 00:09:51 GMT  
		Size: 7.3 MB (7316594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84bdc654760e236b745ad9a4d2b1e74b133d8f882248228d7066303fffeb2f`  
		Last Modified: Sat, 30 Mar 2024 00:10:32 GMT  
		Size: 296.0 MB (296032400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f894c91bf896992cbfb2b9e56a7dced1e2d35df03e4dd4f5448a216b9542bf`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e426cb77616c254e7db9237ea878cb832b26a2f771fb4d9b734b1591ff9e1f`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199881cfb001f502444bcb12a689ba4a7f07983c266fed42a274250c52a887fc`  
		Last Modified: Sat, 30 Mar 2024 00:09:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:f56420e5cb1637937b66aeec6f4bb994a92f6c1e6fda787264025d0ae6b56db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:622e0c5c0660619869931674abfae5c68f0a142a1e4e29d8d5cd4a95aadfa571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231960656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d487ef50e24010e2c38c64389b3abc14813bc46d8acfd4921bd13a7ebfd61b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_VERSION=4.2.24-24
# Tue, 16 Apr 2024 20:16:49 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:17:46 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:17:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:17:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:17:47 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:17:48 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:17:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:17:53 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:17:53 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:17:53 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:17:53 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:17:53 GMT
USER 1001
# Tue, 16 Apr 2024 20:17:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c266668bb7b12d97bb1e32be623f68c14465c80b553d6a292d727cc9ac3d3a5c`  
		Last Modified: Tue, 16 Apr 2024 20:20:59 GMT  
		Size: 4.3 MB (4297902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6ebaec9c8a51be468a06069bce2502d55d3bc2040062f43126d7791953695`  
		Last Modified: Tue, 16 Apr 2024 20:21:13 GMT  
		Size: 117.8 MB (117774151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e053ac5e54f4c54d4320515a01a3f19944bbe986810d31d5be066690f11d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:58 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc29878d09537ef56ffe6c6185c5b679d48f4ed1569f5d7b5ab7786a5ce0f3d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6bbe41c784ec26a42c7b0511e7a1bfd70445d361599c61e68ff77e3653ea5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795aef1b4e64bf3e705358d897b49cb0773a74d319c2deffcaa8d5d9ea32e62`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1954f0407108cf4b93adfd88292ecdafb1b476e76cf8e39044a50672764592e`  
		Last Modified: Tue, 16 Apr 2024 20:20:57 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad166018617a7e45fd76058081d4bc368aa94373a8cb7a19d713cf2fcee796`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:f56420e5cb1637937b66aeec6f4bb994a92f6c1e6fda787264025d0ae6b56db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:622e0c5c0660619869931674abfae5c68f0a142a1e4e29d8d5cd4a95aadfa571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231960656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d487ef50e24010e2c38c64389b3abc14813bc46d8acfd4921bd13a7ebfd61b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_VERSION=4.2.24-24
# Tue, 16 Apr 2024 20:16:49 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:17:46 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:17:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:17:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:17:47 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:17:48 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:17:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:17:53 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:17:53 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:17:53 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:17:53 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:17:53 GMT
USER 1001
# Tue, 16 Apr 2024 20:17:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c266668bb7b12d97bb1e32be623f68c14465c80b553d6a292d727cc9ac3d3a5c`  
		Last Modified: Tue, 16 Apr 2024 20:20:59 GMT  
		Size: 4.3 MB (4297902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6ebaec9c8a51be468a06069bce2502d55d3bc2040062f43126d7791953695`  
		Last Modified: Tue, 16 Apr 2024 20:21:13 GMT  
		Size: 117.8 MB (117774151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e053ac5e54f4c54d4320515a01a3f19944bbe986810d31d5be066690f11d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:58 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc29878d09537ef56ffe6c6185c5b679d48f4ed1569f5d7b5ab7786a5ce0f3d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6bbe41c784ec26a42c7b0511e7a1bfd70445d361599c61e68ff77e3653ea5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795aef1b4e64bf3e705358d897b49cb0773a74d319c2deffcaa8d5d9ea32e62`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1954f0407108cf4b93adfd88292ecdafb1b476e76cf8e39044a50672764592e`  
		Last Modified: Tue, 16 Apr 2024 20:20:57 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad166018617a7e45fd76058081d4bc368aa94373a8cb7a19d713cf2fcee796`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:5b8a01325eaf7b1554e8d56767fc4928e9a6390826746116d85c262a10b50c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:9802cb8b6fd763b91b905cb08172d9cd3df538cdd6d864519792ce1ffd3f2be3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38911558e4a7c525072fee3a730ca16ece26e8150d38cb65c29b893a1654068a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_VERSION=4.4.22-21
# Tue, 16 Apr 2024 20:15:39 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:35 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:16:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:16:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:16:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:16:37 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:16:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:16:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:16:42 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:16:43 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:16:43 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Tue, 16 Apr 2024 20:16:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:16:43 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:16:43 GMT
USER 1001
# Tue, 16 Apr 2024 20:16:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e6b154e5c9a7239842022b618c96b2eb9c3d4e336c5e5c7ce570520c00d481`  
		Last Modified: Tue, 16 Apr 2024 20:20:46 GMT  
		Size: 136.3 MB (136292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f2a17fd8a1031cf0cafeafdd51d756ef351523e86cd29346574838830e18e0`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff7d255661a520d7d1980d71a5e983a28dd790bc6f1984fdc504c7818b0966`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a960df54a5e0b7ebb0e8bea1a8e5bec0a33e66e553a86bedcfadda721206ec`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b176072f3e9badf0c33f65fa2b6ea846b92099783bb6a1409e5d8c1d835d39cd`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 914.5 KB (914541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ef27e48b3024c48119cd6369ef32f5b495ca7dad625d080ec50bc17ec8737`  
		Last Modified: Tue, 16 Apr 2024 20:20:28 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3e3b3df285ae10dade831714414f3d34a3cb7f2a9ad4f233dd7462264dbe5`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c05b7bd9870df5026cf9cb0d5044d5f39368c2e142ffb8378fd05cf8d1a1f95`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:5b8a01325eaf7b1554e8d56767fc4928e9a6390826746116d85c262a10b50c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:9802cb8b6fd763b91b905cb08172d9cd3df538cdd6d864519792ce1ffd3f2be3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38911558e4a7c525072fee3a730ca16ece26e8150d38cb65c29b893a1654068a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_VERSION=4.4.22-21
# Tue, 16 Apr 2024 20:15:39 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:35 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:16:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:16:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:16:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:16:37 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:16:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:16:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:16:42 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:16:43 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:16:43 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Tue, 16 Apr 2024 20:16:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:16:43 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:16:43 GMT
USER 1001
# Tue, 16 Apr 2024 20:16:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e6b154e5c9a7239842022b618c96b2eb9c3d4e336c5e5c7ce570520c00d481`  
		Last Modified: Tue, 16 Apr 2024 20:20:46 GMT  
		Size: 136.3 MB (136292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f2a17fd8a1031cf0cafeafdd51d756ef351523e86cd29346574838830e18e0`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff7d255661a520d7d1980d71a5e983a28dd790bc6f1984fdc504c7818b0966`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a960df54a5e0b7ebb0e8bea1a8e5bec0a33e66e553a86bedcfadda721206ec`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b176072f3e9badf0c33f65fa2b6ea846b92099783bb6a1409e5d8c1d835d39cd`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 914.5 KB (914541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ef27e48b3024c48119cd6369ef32f5b495ca7dad625d080ec50bc17ec8737`  
		Last Modified: Tue, 16 Apr 2024 20:20:28 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3e3b3df285ae10dade831714414f3d34a3cb7f2a9ad4f233dd7462264dbe5`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c05b7bd9870df5026cf9cb0d5044d5f39368c2e142ffb8378fd05cf8d1a1f95`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:ac9b7b4fe32b5d1d0625f9b3b645fbcd3ebb277ffc47d16efe5c6fb6c4728c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:a83b0081a62c869129be72bb2153f8929a76afd9cd220c7c60d528f806774e9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263081584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08174fef1aad95f5686cf07f9db30661b7f4009e9e38a5282c55a16d0bbfc444`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:14:29 GMT
ENV PSMDB_VERSION=5.0.18-15
# Tue, 16 Apr 2024 20:14:29 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:14:29 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Tue, 16 Apr 2024 20:14:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:14:29 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:15:25 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:15:26 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:15:26 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:15:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:15:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:15:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:15:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:15:32 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:15:33 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:15:33 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:15:33 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:15:33 GMT
USER 1001
# Tue, 16 Apr 2024 20:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea51b8751c9d7bc6a589941e79457d40e48ee1498c05b67c90d18428553077`  
		Last Modified: Tue, 16 Apr 2024 20:20:18 GMT  
		Size: 148.9 MB (148895504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7865765d06c2068a5d9646e2d323b3ff853de75f54b8ce99e36799bbefedfb18`  
		Last Modified: Tue, 16 Apr 2024 20:19:44 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a8c5f3416f5c46ba72684f80bd735fca8f46e900016b24cf4ef0efe2d8c9cc`  
		Last Modified: Tue, 16 Apr 2024 20:19:44 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2d49c34f385c8ed9f51326b39febb033cdd587bf928f94fc0260f1580f478`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a681e3d4feaa6a6b99765a67f7242e7f8660b12ffda928aa6b1e297bb6e6c576`  
		Last Modified: Tue, 16 Apr 2024 20:19:43 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1495813d1c861fbd8a75436d2f477b8c40651888b15f32e3478ef44ecf6d33ab`  
		Last Modified: Tue, 16 Apr 2024 20:19:43 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03508c38eff22ea39b85db2b16394f4a1d042bb43687852a6abf8a595e5b2f1b`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e296131fbb9bf0fae0b885c82c507abd7c04af883794583ff5f61f320db2fa`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:ac9b7b4fe32b5d1d0625f9b3b645fbcd3ebb277ffc47d16efe5c6fb6c4728c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:a83b0081a62c869129be72bb2153f8929a76afd9cd220c7c60d528f806774e9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263081584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08174fef1aad95f5686cf07f9db30661b7f4009e9e38a5282c55a16d0bbfc444`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:14:29 GMT
ENV PSMDB_VERSION=5.0.18-15
# Tue, 16 Apr 2024 20:14:29 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:14:29 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Tue, 16 Apr 2024 20:14:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:14:29 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:15:25 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:15:26 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:15:26 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:15:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:15:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:15:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:15:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:15:32 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:15:33 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:15:33 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:15:33 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:15:33 GMT
USER 1001
# Tue, 16 Apr 2024 20:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea51b8751c9d7bc6a589941e79457d40e48ee1498c05b67c90d18428553077`  
		Last Modified: Tue, 16 Apr 2024 20:20:18 GMT  
		Size: 148.9 MB (148895504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7865765d06c2068a5d9646e2d323b3ff853de75f54b8ce99e36799bbefedfb18`  
		Last Modified: Tue, 16 Apr 2024 20:19:44 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a8c5f3416f5c46ba72684f80bd735fca8f46e900016b24cf4ef0efe2d8c9cc`  
		Last Modified: Tue, 16 Apr 2024 20:19:44 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2d49c34f385c8ed9f51326b39febb033cdd587bf928f94fc0260f1580f478`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a681e3d4feaa6a6b99765a67f7242e7f8660b12ffda928aa6b1e297bb6e6c576`  
		Last Modified: Tue, 16 Apr 2024 20:19:43 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1495813d1c861fbd8a75436d2f477b8c40651888b15f32e3478ef44ecf6d33ab`  
		Last Modified: Tue, 16 Apr 2024 20:19:43 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03508c38eff22ea39b85db2b16394f4a1d042bb43687852a6abf8a595e5b2f1b`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e296131fbb9bf0fae0b885c82c507abd7c04af883794583ff5f61f320db2fa`  
		Last Modified: Tue, 16 Apr 2024 20:19:42 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:58676fc4303bdecf42b402abd31e1e85b7efc7c84986aea5ef8ea03997bcdfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:f3c24eccfe3b172846a09319f8254f085583cccf281566108978a55912c6b7f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286601164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a039a844dc9f9571f19ce5a069aaf3579dda507c01cbffa876b6041910d17c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_VERSION=6.0.6-5
# Tue, 16 Apr 2024 20:13:08 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:14:09 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:14:10 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:14:10 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:14:11 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:14:11 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:14:14 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:14:17 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:14:17 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:14:18 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:14:18 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:14:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:14:18 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:14:18 GMT
USER 1001
# Tue, 16 Apr 2024 20:14:18 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d73aa4befa484597fad79fbb905cd7f103bc0dfd722218db6ed0094b1dc84`  
		Last Modified: Tue, 16 Apr 2024 20:19:33 GMT  
		Size: 172.4 MB (172415071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e716128b57e033cd653a81d513c6fc86943a623bfeebc81efc43c6cc0a70c0b`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e641f1b7f359a361bf177ca716e11afcc03f62c770f648e931c3b25cfaae5eb`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db0e924c00454605d5664d9abd47b7dfab1f575c8d5090f78a9249882d652d9`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996fdd354c6335920e9f1b69e986c2690510b9a0c694e725bf042f1ed56abe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:10 GMT  
		Size: 914.5 KB (914542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833df4971b3a1c37a1511aa540ff894bc12c70202608f3063f4c46e053d14fe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 8.1 MB (8137884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed78326a8fa0cee7fc1fac45dcb82b8b888909bde2c128e6be977cdcce95d5a4`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4f19e572ff0cf149a63fd0bde758415002cf5abb55c7c8e4e263f22733210b`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:58676fc4303bdecf42b402abd31e1e85b7efc7c84986aea5ef8ea03997bcdfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:f3c24eccfe3b172846a09319f8254f085583cccf281566108978a55912c6b7f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286601164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a039a844dc9f9571f19ce5a069aaf3579dda507c01cbffa876b6041910d17c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_VERSION=6.0.6-5
# Tue, 16 Apr 2024 20:13:08 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:14:09 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:14:10 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:14:10 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:14:11 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:14:11 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:14:14 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:14:17 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:14:17 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:14:18 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:14:18 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:14:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:14:18 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:14:18 GMT
USER 1001
# Tue, 16 Apr 2024 20:14:18 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d73aa4befa484597fad79fbb905cd7f103bc0dfd722218db6ed0094b1dc84`  
		Last Modified: Tue, 16 Apr 2024 20:19:33 GMT  
		Size: 172.4 MB (172415071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e716128b57e033cd653a81d513c6fc86943a623bfeebc81efc43c6cc0a70c0b`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e641f1b7f359a361bf177ca716e11afcc03f62c770f648e931c3b25cfaae5eb`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db0e924c00454605d5664d9abd47b7dfab1f575c8d5090f78a9249882d652d9`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996fdd354c6335920e9f1b69e986c2690510b9a0c694e725bf042f1ed56abe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:10 GMT  
		Size: 914.5 KB (914542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833df4971b3a1c37a1511aa540ff894bc12c70202608f3063f4c46e053d14fe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 8.1 MB (8137884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed78326a8fa0cee7fc1fac45dcb82b8b888909bde2c128e6be977cdcce95d5a4`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4f19e572ff0cf149a63fd0bde758415002cf5abb55c7c8e4e263f22733210b`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
