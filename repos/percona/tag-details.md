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
-	[`percona:8.0.35-27`](#percona8035-27)
-	[`percona:8.0.35-27-centos`](#percona8035-27-centos)
-	[`percona:centos`](#perconacentos)
-	[`percona:ps-5`](#perconaps-5)
-	[`percona:ps-5.6`](#perconaps-56)
-	[`percona:ps-5.6.51-2`](#perconaps-5651-2)
-	[`percona:ps-5.7`](#perconaps-57)
-	[`percona:ps-5.7.44`](#perconaps-5744)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.35-27`](#perconaps-8035-27)
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
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
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
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.35-27`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.35-27` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.35-27-centos`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.35-27-centos` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
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
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:1701d36c5ef9fb895d6a5df927bf6ae599e7d460022a9f1dd836a66a75b2c416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:6fcac2a9a68a97073fe11d8a86e0dac1eea0187b739426df0e9bf65190c0f4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454079125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aebaea1191157de8bf0e6c327b124594a9af78ba8a1c8b3c2cfde826e0e84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:23:14 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 14 Feb 2024 03:23:56 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:23:57 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:24:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:24:39 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 14 Feb 2024 03:24:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:24:40 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:24:40 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 14 Feb 2024 03:24:40 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:24:40 GMT
USER mysql
# Wed, 14 Feb 2024 03:24:40 GMT
EXPOSE 3306
# Wed, 14 Feb 2024 03:24:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78300c0ca77a830dcce19848896c6f81d5f7d06130f1a76d39a375bca63695b2`  
		Last Modified: Wed, 14 Feb 2024 03:31:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a10a0e4fb3796258f6f63c37f89b48181973d06118aaa280516fcc9578e3c`  
		Last Modified: Wed, 14 Feb 2024 03:31:23 GMT  
		Size: 215.2 MB (215155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc821f0e470c814f4edab7f29da86699ba9914f46b339518b437d206716e52`  
		Last Modified: Wed, 14 Feb 2024 03:31:31 GMT  
		Size: 138.1 MB (138136193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c64c8d0a940a891f4b11ae2e1f721bc3ab0f9c2ea38b3b6e62a7ad716b25f`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8563da649d3c9d2d58dea1da4e2a8e2cfbbe14abb02d7b2ce29f012435dff`  
		Last Modified: Wed, 14 Feb 2024 03:31:11 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80880461cfa9a1e1b7f195cca58210e13dfe0797faa6ba4856bb5b9b223856bd`  
		Last Modified: Wed, 14 Feb 2024 03:31:12 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.35-27`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.35-27` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:5a5c9e889081e0cac3e2116951e2a0bc8e2809262bf5c661f5776b55bbecee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c274ae688bf7b2f95aa14b99f54a502e5db323e30c887aef3693eb72efbcb24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231912624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13493a7a6f4f46d289a273d9d5b8b52784c8c4395d685f2e32b736cccd871310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 14 Feb 2024 03:28:38 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:41 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:29:36 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:29:37 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:29:37 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:29:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:29:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:29:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:29:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:29:44 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:29:44 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:29:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:29:44 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:29:44 GMT
USER 1001
# Wed, 14 Feb 2024 03:29:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f781da700ea39955e4ea9ec1e17f5f8437eb6ac396f642e025a076560b238c3`  
		Last Modified: Wed, 14 Feb 2024 03:33:34 GMT  
		Size: 4.3 MB (4284789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee3cbbb76419628836111775ef32c3c6f0d067128b18c9356d8d1e31242b974`  
		Last Modified: Wed, 14 Feb 2024 03:33:48 GMT  
		Size: 117.8 MB (117763846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2b5ff6f294b62e2d06e0b5c56de239bab99c067753a435fc44d1b62ea35756`  
		Last Modified: Wed, 14 Feb 2024 03:33:33 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47a4b8e9f0a803d831fe502933a1d5c981517d2d23b1401a15ba1be9fc0bd21`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a3d3b3ebfd47bf9a4ce00ae83eb845079fee1d6e0eb98c628233386aa83d57`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee85faeba83c42b64c728e732cb64e43b14d51382119724b558927e879926e9`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709167988c9838150e205539cd49e134273c668000f7c72d293342d81614cba2`  
		Last Modified: Wed, 14 Feb 2024 03:33:32 GMT  
		Size: 8.2 MB (8151449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b710d0eead90f56936c44562524a23137efcbeaf6576281ea2203eb89c42642c`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:5a5c9e889081e0cac3e2116951e2a0bc8e2809262bf5c661f5776b55bbecee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:c274ae688bf7b2f95aa14b99f54a502e5db323e30c887aef3693eb72efbcb24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231912624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13493a7a6f4f46d289a273d9d5b8b52784c8c4395d685f2e32b736cccd871310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 14 Feb 2024 03:28:38 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:41 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:29:36 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:29:37 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:29:37 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:29:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:29:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:29:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:29:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:29:44 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:29:44 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:29:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:29:44 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:29:44 GMT
USER 1001
# Wed, 14 Feb 2024 03:29:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f781da700ea39955e4ea9ec1e17f5f8437eb6ac396f642e025a076560b238c3`  
		Last Modified: Wed, 14 Feb 2024 03:33:34 GMT  
		Size: 4.3 MB (4284789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee3cbbb76419628836111775ef32c3c6f0d067128b18c9356d8d1e31242b974`  
		Last Modified: Wed, 14 Feb 2024 03:33:48 GMT  
		Size: 117.8 MB (117763846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2b5ff6f294b62e2d06e0b5c56de239bab99c067753a435fc44d1b62ea35756`  
		Last Modified: Wed, 14 Feb 2024 03:33:33 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47a4b8e9f0a803d831fe502933a1d5c981517d2d23b1401a15ba1be9fc0bd21`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a3d3b3ebfd47bf9a4ce00ae83eb845079fee1d6e0eb98c628233386aa83d57`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee85faeba83c42b64c728e732cb64e43b14d51382119724b558927e879926e9`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709167988c9838150e205539cd49e134273c668000f7c72d293342d81614cba2`  
		Last Modified: Wed, 14 Feb 2024 03:33:32 GMT  
		Size: 8.2 MB (8151449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b710d0eead90f56936c44562524a23137efcbeaf6576281ea2203eb89c42642c`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:80a277c1b7dfc548010b846033f933e280640933d81c4d0d19bff436db86d720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:ea06d087f06615150392b66f6d8c0e98c0a6accb28b63a6533562d91fd8c6fb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250434813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790c991636a0c8a6ff7d70f7d3f2ac924a133024e71c6a7e7033fe3b5ca7d008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:27:28 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 14 Feb 2024 03:27:28 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:27:29 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:25 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:28:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:28:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:28:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:28:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:28:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:28:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:28:33 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:28:33 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:28:33 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 14 Feb 2024 03:28:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:28:33 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:28:34 GMT
USER 1001
# Wed, 14 Feb 2024 03:28:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fa19d905aa99ba03d189d271de8f76a01a350d79e076f32f19f9802bbdaf53`  
		Last Modified: Wed, 14 Feb 2024 03:33:18 GMT  
		Size: 136.3 MB (136286392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c933f44d6aac23894f5b914e5462d67c1f5f6d8e8db146a6fa29e7398f369fd9`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71366c442dfc0533125b82c245b122beb75a12e6f3038b6f3094bf3d84cba305`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b41615400a587cd4cb81cbd19927f9916727266fe6d816a3839159fd6bd26`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52de67cbb1d76190666fa4b9dd622edc7f6d3cd04c40b16be7e63c94800aa6f3`  
		Last Modified: Wed, 14 Feb 2024 03:33:00 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d829bc6a1a3eec0a7da09b157172189688cb384099d413b5e873fbefe25e0c71`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f3832ba9b5af8c62acf1b0fbc97203fc425fa6a827d29f7bc398234b0db139`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8f4fb82711a2af6325d75404b4c995dd72754bfb1fa3a23ec84c6e3a234369`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:80a277c1b7dfc548010b846033f933e280640933d81c4d0d19bff436db86d720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:ea06d087f06615150392b66f6d8c0e98c0a6accb28b63a6533562d91fd8c6fb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250434813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790c991636a0c8a6ff7d70f7d3f2ac924a133024e71c6a7e7033fe3b5ca7d008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:27:28 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 14 Feb 2024 03:27:28 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:27:29 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:25 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:28:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:28:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:28:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:28:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:28:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:28:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:28:33 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:28:33 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:28:33 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 14 Feb 2024 03:28:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:28:33 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:28:34 GMT
USER 1001
# Wed, 14 Feb 2024 03:28:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fa19d905aa99ba03d189d271de8f76a01a350d79e076f32f19f9802bbdaf53`  
		Last Modified: Wed, 14 Feb 2024 03:33:18 GMT  
		Size: 136.3 MB (136286392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c933f44d6aac23894f5b914e5462d67c1f5f6d8e8db146a6fa29e7398f369fd9`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71366c442dfc0533125b82c245b122beb75a12e6f3038b6f3094bf3d84cba305`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b41615400a587cd4cb81cbd19927f9916727266fe6d816a3839159fd6bd26`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52de67cbb1d76190666fa4b9dd622edc7f6d3cd04c40b16be7e63c94800aa6f3`  
		Last Modified: Wed, 14 Feb 2024 03:33:00 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d829bc6a1a3eec0a7da09b157172189688cb384099d413b5e873fbefe25e0c71`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f3832ba9b5af8c62acf1b0fbc97203fc425fa6a827d29f7bc398234b0db139`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8f4fb82711a2af6325d75404b4c995dd72754bfb1fa3a23ec84c6e3a234369`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:e726939332e2dae90eff882c0a1c90eecbb14db8288649fda6b631a4070e13d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:8089f9e18d0c055beb51984c9cedeb1a50f284f3ad89fe6cab2630a6e810d30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263043504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765607bcb8e87b7ad0471ca366da2bae2766dc47b98ae74238d4d0cffbba649e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 14 Feb 2024 03:26:18 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:27:17 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:27:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:27:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:27:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:27:19 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:27:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:27:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:27:24 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:27:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:27:25 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:27:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:27:25 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:27:25 GMT
USER 1001
# Wed, 14 Feb 2024 03:27:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5fff3254479387f2542bbf5b9e32b0ed20c5c6b650fd0bb9373ff1c0d81deb`  
		Last Modified: Wed, 14 Feb 2024 03:32:50 GMT  
		Size: 148.9 MB (148895087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addcec4c3400336e13aedc295a8c60e3af45c1beabde402f808527973eb5f419`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deb95d882df26ca2ec93d6aca72133408caa6c2188c5390cf7aac73e1a3e5e8`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42197984ee26fef93e92f7fb541ccb6159c85dc6ab4db6fd28fc97397696d5b2`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac12d2cbb4f0db619a1e20221ba2c242bf9a959f6838d77cf739bc43d4e1bc1`  
		Last Modified: Wed, 14 Feb 2024 03:32:31 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aab4c6450b63153888c1b2bef0daca57ea7ac840adbac952362b07b3edf657`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417b6e04893106d0c9c0eb8aee46c068ae2d8fd1d0332b64345340e7dd10a1cd`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee85fc0166b1f4d18cb07ca260ae4014bd6454b998d4796bec7599aacfcc4ab`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:e726939332e2dae90eff882c0a1c90eecbb14db8288649fda6b631a4070e13d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:8089f9e18d0c055beb51984c9cedeb1a50f284f3ad89fe6cab2630a6e810d30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263043504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765607bcb8e87b7ad0471ca366da2bae2766dc47b98ae74238d4d0cffbba649e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 14 Feb 2024 03:26:18 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:27:17 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:27:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:27:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:27:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:27:19 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:27:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:27:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:27:24 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:27:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:27:25 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:27:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:27:25 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:27:25 GMT
USER 1001
# Wed, 14 Feb 2024 03:27:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5fff3254479387f2542bbf5b9e32b0ed20c5c6b650fd0bb9373ff1c0d81deb`  
		Last Modified: Wed, 14 Feb 2024 03:32:50 GMT  
		Size: 148.9 MB (148895087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addcec4c3400336e13aedc295a8c60e3af45c1beabde402f808527973eb5f419`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deb95d882df26ca2ec93d6aca72133408caa6c2188c5390cf7aac73e1a3e5e8`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42197984ee26fef93e92f7fb541ccb6159c85dc6ab4db6fd28fc97397696d5b2`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac12d2cbb4f0db619a1e20221ba2c242bf9a959f6838d77cf739bc43d4e1bc1`  
		Last Modified: Wed, 14 Feb 2024 03:32:31 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aab4c6450b63153888c1b2bef0daca57ea7ac840adbac952362b07b3edf657`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417b6e04893106d0c9c0eb8aee46c068ae2d8fd1d0332b64345340e7dd10a1cd`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee85fc0166b1f4d18cb07ca260ae4014bd6454b998d4796bec7599aacfcc4ab`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:b62961d6fa30ed4fdfaa5445f28d175d240be2119d5da9feb6b073fb45669200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:a40704f86547638baf26e5f76dec951295b949f0be01bfe79ceb9398a50670df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286511320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b6e0acd7d05e8aaf4eebff64d83ff2352ce2248601761bbf7034864118199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 14 Feb 2024 03:24:57 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:25:59 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:26:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:26:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:26:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:26:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:26:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:26:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:26:07 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:26:08 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:26:08 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:26:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:26:08 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:26:08 GMT
USER 1001
# Wed, 14 Feb 2024 03:26:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021060124ad80bd190033661eaa52f28cc0c8d2f73c8865f4e19f064ad502c5d`  
		Last Modified: Wed, 14 Feb 2024 03:32:20 GMT  
		Size: 172.4 MB (172362902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34122ae3a48402e105e6d02affaa2cc4ab29eced6bf81368ad50929e29dbb859`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79971bb90e407b13cd886932f000527230661fef66102db330bf28238bb6e6c`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7300dbfb55a78a98561980ea5a0d6abd0d218ce3ec312597b269ba5cafc99`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0c3b7de4605dd0f7f2ed94e5b1782142c37f07bf87f3440c6b389ecf0d910d`  
		Last Modified: Wed, 14 Feb 2024 03:31:58 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0612d258b9afd71352eba793c7c12344cacf6095f74ceafcb9d3e671c11e84df`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cf75a2ec34bc4d09a4232e739246cc8bad8ceb9dfaaf50d0812831fd062dc`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe407e9a21d928d87b9c89c8937e97faa47ff55c9eabaf79c3d606b6c96f29d9`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:b62961d6fa30ed4fdfaa5445f28d175d240be2119d5da9feb6b073fb45669200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:a40704f86547638baf26e5f76dec951295b949f0be01bfe79ceb9398a50670df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286511320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b6e0acd7d05e8aaf4eebff64d83ff2352ce2248601761bbf7034864118199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 14 Feb 2024 03:24:57 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:25:59 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:26:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:26:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:26:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:26:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:26:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:26:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:26:07 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:26:08 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:26:08 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:26:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:26:08 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:26:08 GMT
USER 1001
# Wed, 14 Feb 2024 03:26:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021060124ad80bd190033661eaa52f28cc0c8d2f73c8865f4e19f064ad502c5d`  
		Last Modified: Wed, 14 Feb 2024 03:32:20 GMT  
		Size: 172.4 MB (172362902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34122ae3a48402e105e6d02affaa2cc4ab29eced6bf81368ad50929e29dbb859`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79971bb90e407b13cd886932f000527230661fef66102db330bf28238bb6e6c`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7300dbfb55a78a98561980ea5a0d6abd0d218ce3ec312597b269ba5cafc99`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0c3b7de4605dd0f7f2ed94e5b1782142c37f07bf87f3440c6b389ecf0d910d`  
		Last Modified: Wed, 14 Feb 2024 03:31:58 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0612d258b9afd71352eba793c7c12344cacf6095f74ceafcb9d3e671c11e84df`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cf75a2ec34bc4d09a4232e739246cc8bad8ceb9dfaaf50d0812831fd062dc`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe407e9a21d928d87b9c89c8937e97faa47ff55c9eabaf79c3d606b6c96f29d9`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
