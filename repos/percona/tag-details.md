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
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
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
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.35-27`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.35-27` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.35-27-centos`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.35-27-centos` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
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
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.35-27`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.35-27` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:ea26cc24ad333ce9fe56676ea259075086bf978d92b063c6e0284b33b146ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:e397d712b08f282ad17a8c6e2037824224caa7b7d354d3bcdde1c7ff421c10f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d022327686822f0c31fa4b94f86bb7ff6f81f38ea9018da72e1b91c6962dc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 07 Feb 2024 06:47:59 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:48:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:48:53 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:48:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:48:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:48:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:48:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:48:57 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:48:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:48:59 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:49:00 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:49:00 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:49:00 GMT
USER 1001
# Wed, 07 Feb 2024 06:49:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a0b9e9b323f60e06123587564f7434c314c9d4c88fdfda35720e3283ac60a6`  
		Last Modified: Wed, 07 Feb 2024 06:52:52 GMT  
		Size: 4.3 MB (4284815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e256ffe9a34138e4c7c1ce0dcd0d046890e5337dc5f42542209b95f0c0799676`  
		Last Modified: Wed, 07 Feb 2024 06:53:07 GMT  
		Size: 117.8 MB (117771565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721f24a6becf3b86961fc631beb3e6d73aba0d7f85fd973f31fd0eb08e33ed9c`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d06c9e4d282ee43c01ce1f7c932c4e1c3fb42f208466643ba08fc3f11f51fda`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baab55a76002db3549569d20690cf8a4e14e513abb294081a6a7be9c63fa373`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f18540912b57be71ab04c088fbcb874600fd7dd100b19e90a90fdd49f1aa1be`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119da7b07afd289e9b848676fbce724efb65f98d0ea000e114862ef2360daa4f`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 8.2 MB (8151455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4094cb03a3d5b98484f838abbbd039ed2fb4cc19ab200f74bf501ab0aa524842`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:ea26cc24ad333ce9fe56676ea259075086bf978d92b063c6e0284b33b146ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:e397d712b08f282ad17a8c6e2037824224caa7b7d354d3bcdde1c7ff421c10f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d022327686822f0c31fa4b94f86bb7ff6f81f38ea9018da72e1b91c6962dc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 07 Feb 2024 06:47:59 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:48:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:48:53 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:48:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:48:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:48:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:48:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:48:57 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:48:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:48:59 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:49:00 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:49:00 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:49:00 GMT
USER 1001
# Wed, 07 Feb 2024 06:49:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a0b9e9b323f60e06123587564f7434c314c9d4c88fdfda35720e3283ac60a6`  
		Last Modified: Wed, 07 Feb 2024 06:52:52 GMT  
		Size: 4.3 MB (4284815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e256ffe9a34138e4c7c1ce0dcd0d046890e5337dc5f42542209b95f0c0799676`  
		Last Modified: Wed, 07 Feb 2024 06:53:07 GMT  
		Size: 117.8 MB (117771565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721f24a6becf3b86961fc631beb3e6d73aba0d7f85fd973f31fd0eb08e33ed9c`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d06c9e4d282ee43c01ce1f7c932c4e1c3fb42f208466643ba08fc3f11f51fda`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baab55a76002db3549569d20690cf8a4e14e513abb294081a6a7be9c63fa373`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f18540912b57be71ab04c088fbcb874600fd7dd100b19e90a90fdd49f1aa1be`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119da7b07afd289e9b848676fbce724efb65f98d0ea000e114862ef2360daa4f`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 8.2 MB (8151455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4094cb03a3d5b98484f838abbbd039ed2fb4cc19ab200f74bf501ab0aa524842`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:fbb7b8b3194178bb00214d9ec9a98fa7188c7b6c352dce310f9650740922e85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:135bf1811ec5d68050294e6caa22664ac703695752acb8b411defe18fcff7b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250431966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33be95a2099537cc8e194d8e6e8f59b2f65937cb7ef827283e2654a9b1690891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:46:49 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 07 Feb 2024 06:46:49 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:46:49 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 07 Feb 2024 06:46:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:46:49 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:47:42 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:47:43 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:47:43 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:47:44 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:47:44 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:47:47 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:47:49 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:47:50 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:47:50 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:47:50 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 07 Feb 2024 06:47:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:47:51 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:47:51 GMT
USER 1001
# Wed, 07 Feb 2024 06:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2957e50ca955fcb56385f9223470b1079b6f73f78633c1bfe784fb2b266b551`  
		Last Modified: Wed, 07 Feb 2024 06:52:40 GMT  
		Size: 136.3 MB (136277384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8f71b73dbc804f15f9e70bca3b96705839c1dd319aa77b235f1f130b3e409d`  
		Last Modified: Wed, 07 Feb 2024 06:52:21 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6da854fbd3fd14fbb14323d2dcc7ef14e17d5bc9bc033566f6c915546d3c19`  
		Last Modified: Wed, 07 Feb 2024 06:52:21 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0b803871e94b202f223f5123edb7e1ce39e67db859100fdac495d060e3f118`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367a6797456eb5c2c6321ff7cc4e1c6b186e6bcf404bd6fa871d50e4fc967820`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa886d90211ad363d59d5a7f5a1bc3099dc5188979c7627a2c825970b2d642`  
		Last Modified: Wed, 07 Feb 2024 06:52:20 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb13b29e90ea6665a2f7dce0f466f336c5ca5e60b0fdbf50baae4d24e82bf58`  
		Last Modified: Wed, 07 Feb 2024 06:52:18 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40319dd189c52f7243fc3c0b3cc32509e79c766071229fc1e46438f447487dfc`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:fbb7b8b3194178bb00214d9ec9a98fa7188c7b6c352dce310f9650740922e85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:135bf1811ec5d68050294e6caa22664ac703695752acb8b411defe18fcff7b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250431966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33be95a2099537cc8e194d8e6e8f59b2f65937cb7ef827283e2654a9b1690891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:46:49 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 07 Feb 2024 06:46:49 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:46:49 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 07 Feb 2024 06:46:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:46:49 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:47:42 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:47:43 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:47:43 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:47:44 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:47:44 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:47:47 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:47:49 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:47:50 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:47:50 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:47:50 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 07 Feb 2024 06:47:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:47:51 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:47:51 GMT
USER 1001
# Wed, 07 Feb 2024 06:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2957e50ca955fcb56385f9223470b1079b6f73f78633c1bfe784fb2b266b551`  
		Last Modified: Wed, 07 Feb 2024 06:52:40 GMT  
		Size: 136.3 MB (136277384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8f71b73dbc804f15f9e70bca3b96705839c1dd319aa77b235f1f130b3e409d`  
		Last Modified: Wed, 07 Feb 2024 06:52:21 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6da854fbd3fd14fbb14323d2dcc7ef14e17d5bc9bc033566f6c915546d3c19`  
		Last Modified: Wed, 07 Feb 2024 06:52:21 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0b803871e94b202f223f5123edb7e1ce39e67db859100fdac495d060e3f118`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367a6797456eb5c2c6321ff7cc4e1c6b186e6bcf404bd6fa871d50e4fc967820`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa886d90211ad363d59d5a7f5a1bc3099dc5188979c7627a2c825970b2d642`  
		Last Modified: Wed, 07 Feb 2024 06:52:20 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb13b29e90ea6665a2f7dce0f466f336c5ca5e60b0fdbf50baae4d24e82bf58`  
		Last Modified: Wed, 07 Feb 2024 06:52:18 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40319dd189c52f7243fc3c0b3cc32509e79c766071229fc1e46438f447487dfc`  
		Last Modified: Wed, 07 Feb 2024 06:52:19 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:30b578806680d30ab04027072e5e794ceb263ecbca030052072d2141018eab4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:23c97954fa38dff5cbf667e067052b91182021f361bba4f40cf800cdc0a130d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263051645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b143dd56e1794267ad2c10a74cf4c2f67b77a637fdc27cf9a6cd5d4ce158bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 07 Feb 2024 06:45:39 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:46:33 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:46:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:46:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:46:35 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:46:35 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:46:38 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:46:40 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:46:40 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:46:41 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:46:41 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:46:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:46:41 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:46:41 GMT
USER 1001
# Wed, 07 Feb 2024 06:46:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70886cf0afd4f86e6071e89c3c757e1713fcf3a396fc2d8b0aab67630f962487`  
		Last Modified: Wed, 07 Feb 2024 06:52:09 GMT  
		Size: 148.9 MB (148897065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9cd589b2134e60f19a1c3eba1a338e82424a1eaf318a79cbe422dbd7834b9e`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7041e03e34ddb7d3cda94fdf1ec2f6c2a9364e5cf64d73839d36aa370f54cfd9`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f730048d553e8b5a9213999f5c9a054ceb3dcebf4422ad8f009b61e319bcfa91`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a485b5dad5105b62b4926b368fed74a00fa67e3ed9c35d41e12eb69875d25`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c297790844148ad2dc1b5a68d02330db5afadeadf53b3cfaea5dfa16b15a5d5b`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a14df46e5359e9eabd6d654e59cb97eebea774edff6e9a5c7e0984a7eea53`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97e96658e3b92b21e60cf796061da2797c2f65791bf5e9581f11755ad36e624`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:30b578806680d30ab04027072e5e794ceb263ecbca030052072d2141018eab4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:23c97954fa38dff5cbf667e067052b91182021f361bba4f40cf800cdc0a130d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263051645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b143dd56e1794267ad2c10a74cf4c2f67b77a637fdc27cf9a6cd5d4ce158bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 07 Feb 2024 06:45:39 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:46:33 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:46:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:46:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:46:35 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:46:35 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:46:38 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:46:40 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:46:40 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:46:41 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:46:41 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:46:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:46:41 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:46:41 GMT
USER 1001
# Wed, 07 Feb 2024 06:46:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70886cf0afd4f86e6071e89c3c757e1713fcf3a396fc2d8b0aab67630f962487`  
		Last Modified: Wed, 07 Feb 2024 06:52:09 GMT  
		Size: 148.9 MB (148897065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9cd589b2134e60f19a1c3eba1a338e82424a1eaf318a79cbe422dbd7834b9e`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7041e03e34ddb7d3cda94fdf1ec2f6c2a9364e5cf64d73839d36aa370f54cfd9`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f730048d553e8b5a9213999f5c9a054ceb3dcebf4422ad8f009b61e319bcfa91`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a485b5dad5105b62b4926b368fed74a00fa67e3ed9c35d41e12eb69875d25`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c297790844148ad2dc1b5a68d02330db5afadeadf53b3cfaea5dfa16b15a5d5b`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a14df46e5359e9eabd6d654e59cb97eebea774edff6e9a5c7e0984a7eea53`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97e96658e3b92b21e60cf796061da2797c2f65791bf5e9581f11755ad36e624`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:243debd7da3af830e55242ab9bcc60867898da56d74d6d32db877e2da320ddf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:55a5dee6851089ae9d2a838840c53305c6f4aadc8ab92a5634a368a8b9496012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a95c29727d4dac037647695f5c42566b478c207e5ce7c4796d9cf0ae51062ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:44:18 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 07 Feb 2024 06:44:18 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:44:18 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 07 Feb 2024 06:44:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:44:18 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:45:17 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:45:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:45:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:45:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:45:19 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:45:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:45:25 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:45:25 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:45:26 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:45:26 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:45:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:45:26 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:45:26 GMT
USER 1001
# Wed, 07 Feb 2024 06:45:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9410d7feae0383f3e0c5f31c1e23e91f4ade9238ba80cb641b547ed17be642`  
		Last Modified: Wed, 07 Feb 2024 06:51:38 GMT  
		Size: 172.4 MB (172372016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a153800223778f87fc989e83f259d3451ab940e27caf0dc7f97adf722093c07`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2e888446db074edf75d7921d9466892637604ca4b9dae933588ccd1b6b7021`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2b9d7e0822de2f0494315cf62c22c7835b33b6a62e8cbd94967479dd80bbd4`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3ae783e97bf46e5c8c7d658ac339663fd8fa046815a93bfe0dbd24a500a0b0`  
		Last Modified: Wed, 07 Feb 2024 06:51:13 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474106c1b70219fb116f79095063f64f32a39d16c4a1fe1ff8d2cb6f0c2b54a8`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 8.1 MB (8137900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc7f20c0f9e1c9865744d05de845fe6aecc7a7290347afa277dd9ffc103a5ee`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8355d06d1a49a574a2b6d2360f837d981c241f10868b05a1fec373ba688ee30d`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:243debd7da3af830e55242ab9bcc60867898da56d74d6d32db877e2da320ddf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:55a5dee6851089ae9d2a838840c53305c6f4aadc8ab92a5634a368a8b9496012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a95c29727d4dac037647695f5c42566b478c207e5ce7c4796d9cf0ae51062ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:44:18 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 07 Feb 2024 06:44:18 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:44:18 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 07 Feb 2024 06:44:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:44:18 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:45:17 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:45:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:45:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:45:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:45:19 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:45:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:45:25 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:45:25 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:45:26 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:45:26 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:45:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:45:26 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:45:26 GMT
USER 1001
# Wed, 07 Feb 2024 06:45:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9410d7feae0383f3e0c5f31c1e23e91f4ade9238ba80cb641b547ed17be642`  
		Last Modified: Wed, 07 Feb 2024 06:51:38 GMT  
		Size: 172.4 MB (172372016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a153800223778f87fc989e83f259d3451ab940e27caf0dc7f97adf722093c07`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2e888446db074edf75d7921d9466892637604ca4b9dae933588ccd1b6b7021`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2b9d7e0822de2f0494315cf62c22c7835b33b6a62e8cbd94967479dd80bbd4`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3ae783e97bf46e5c8c7d658ac339663fd8fa046815a93bfe0dbd24a500a0b0`  
		Last Modified: Wed, 07 Feb 2024 06:51:13 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474106c1b70219fb116f79095063f64f32a39d16c4a1fe1ff8d2cb6f0c2b54a8`  
		Last Modified: Wed, 07 Feb 2024 06:51:14 GMT  
		Size: 8.1 MB (8137900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc7f20c0f9e1c9865744d05de845fe6aecc7a7290347afa277dd9ffc103a5ee`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8355d06d1a49a574a2b6d2360f837d981c241f10868b05a1fec373ba688ee30d`  
		Last Modified: Wed, 07 Feb 2024 06:51:12 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
