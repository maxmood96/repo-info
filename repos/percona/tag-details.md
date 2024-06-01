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
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
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
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
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
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
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
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:31563b629aabe86079bbaf84ed26bd037a795806d7b5f2f9f103f48edc0f042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:9574a4236a7b0b5c8e25be0593fa19d9808a8e8c8e3be16f7ccb0c0981c6427b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.0 MB (473022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd00d71afee3dd7b12ae59fd22e1686d188bfee8fef1e5a6787817bb2f60bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:38:50 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Sat, 01 Jun 2024 01:39:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_VERSION=5.7.44-48.1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Sat, 01 Jun 2024 01:39:32 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Sat, 01 Jun 2024 01:39:32 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Sat, 01 Jun 2024 01:39:33 GMT
ENV CALL_HOME_VERSION=0.1
# Sat, 01 Jun 2024 01:39:33 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Sat, 01 Jun 2024 01:40:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Sat, 01 Jun 2024 01:40:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Sat, 01 Jun 2024 01:40:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Sat, 01 Jun 2024 01:40:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Sat, 01 Jun 2024 01:40:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Sat, 01 Jun 2024 01:40:18 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Sat, 01 Jun 2024 01:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 01 Jun 2024 01:40:18 GMT
USER mysql
# Sat, 01 Jun 2024 01:40:18 GMT
EXPOSE 3306
# Sat, 01 Jun 2024 01:40:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855a58cd4a6b10b4f7c75761acb12e5916347ce69bcbaa9b1f6cbcf6584332b1`  
		Last Modified: Sat, 01 Jun 2024 01:47:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d8a92bcfa5782a964a5656996dbfb24ca0836e92672d25ce5c87c655f517d`  
		Last Modified: Sat, 01 Jun 2024 01:47:12 GMT  
		Size: 234.1 MB (234135526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22e006f6b522abd3c6c95d06ced883a9a390004e8cba7e3330128039315da1`  
		Last Modified: Sat, 01 Jun 2024 01:47:17 GMT  
		Size: 138.2 MB (138190317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd816010a9b8daddca79ef38a8964641d6dc9a384d542d38722b2856b2e0c1`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8509aca9ed9d89d2d8615be0d5afd165e8b4beb3217dbca963d99d029f2218`  
		Last Modified: Sat, 01 Jun 2024 01:47:00 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a14aef561fd76bcc86f4285493e9c10e02bc4dd794f732b6ef721773a3baa`  
		Last Modified: Sat, 01 Jun 2024 01:46:59 GMT  
		Size: 3.3 KB (3289 bytes)  
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
$ docker pull percona@sha256:14a1ed711ca65747a2fc9e2094f6e5d3dea10a6f71985216ae21379fbec0f8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c0ddf1348f8afb33051980d8287fac4599aeb6ccad35463c811cda694b22c02b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231808346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f540a18280135f220950c99ce6acf5a9c28f2a77994d46caa57ec58633291ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 01 Jun 2024 01:44:29 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:45:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:45:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:45:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:45:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:45:28 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:45:32 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:45:35 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:45:36 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:45:36 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:45:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:45:36 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:45:36 GMT
USER 1001
# Sat, 01 Jun 2024 01:45:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08437527b413502ca7d129217ebf1c1219980457fa03f229fd38c3eb1f67c4b5`  
		Last Modified: Sat, 01 Jun 2024 01:49:15 GMT  
		Size: 4.3 MB (4284328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419d86d757489cbad6f23971b617a6abf1d1d067774085bc6b8e2d0f3ea0dd9`  
		Last Modified: Sat, 01 Jun 2024 01:49:29 GMT  
		Size: 117.7 MB (117749999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f975cf23577c288ccdce46292bafdd0ebd2810860d0eca2712011490bc1a2e`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da284916143c4c2331757661e94a880164e62b7c473da85ce7991dc3cc9cbf86`  
		Last Modified: Sat, 01 Jun 2024 01:49:12 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a040cd4b8864caee176cfe2476bdec1bfda8349a320202e6540de82de17dcd3c`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17382e814da8c20d3dc2885769937a943a706d3ba03c25b9c7fca903168685`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7807a633fb4a2ad0e474d173f2c6a0c8751120a1c4b540354a21348f6091d7`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6310d236e1102b5de9fdb27fc35a4f42548e5c0f39c3e96b879c9b8d37839d`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:14a1ed711ca65747a2fc9e2094f6e5d3dea10a6f71985216ae21379fbec0f8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:c0ddf1348f8afb33051980d8287fac4599aeb6ccad35463c811cda694b22c02b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231808346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f540a18280135f220950c99ce6acf5a9c28f2a77994d46caa57ec58633291ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 01 Jun 2024 01:44:29 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:45:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:45:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:45:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:45:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:45:28 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:45:32 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:45:35 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:45:36 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:45:36 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:45:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:45:36 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:45:36 GMT
USER 1001
# Sat, 01 Jun 2024 01:45:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08437527b413502ca7d129217ebf1c1219980457fa03f229fd38c3eb1f67c4b5`  
		Last Modified: Sat, 01 Jun 2024 01:49:15 GMT  
		Size: 4.3 MB (4284328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419d86d757489cbad6f23971b617a6abf1d1d067774085bc6b8e2d0f3ea0dd9`  
		Last Modified: Sat, 01 Jun 2024 01:49:29 GMT  
		Size: 117.7 MB (117749999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f975cf23577c288ccdce46292bafdd0ebd2810860d0eca2712011490bc1a2e`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da284916143c4c2331757661e94a880164e62b7c473da85ce7991dc3cc9cbf86`  
		Last Modified: Sat, 01 Jun 2024 01:49:12 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a040cd4b8864caee176cfe2476bdec1bfda8349a320202e6540de82de17dcd3c`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17382e814da8c20d3dc2885769937a943a706d3ba03c25b9c7fca903168685`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7807a633fb4a2ad0e474d173f2c6a0c8751120a1c4b540354a21348f6091d7`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6310d236e1102b5de9fdb27fc35a4f42548e5c0f39c3e96b879c9b8d37839d`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:2434bdc36f05dd7e07042c6fa7a720124e44be8258272413e0e1a0af5a51f06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:7ce7e1dd021e1ce821e2609d471975c2ac67ee334fe8eee6db8c0d22996f33bf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250330853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee8737267229bfb00293e2a379dfe28a1761c48600c808d4f63f3d929e43e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 01 Jun 2024 01:43:19 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:15 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:44:16 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:44:16 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:44:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:44:17 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:44:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:44:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:44:23 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:44:24 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:44:24 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 01 Jun 2024 01:44:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:44:24 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:44:24 GMT
USER 1001
# Sat, 01 Jun 2024 01:44:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849a437aa8e7437bbfe3be1495bc80750d7fdc26fd505c8ce32ceb970f53d109`  
		Last Modified: Sat, 01 Jun 2024 01:49:04 GMT  
		Size: 136.3 MB (136272862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bdb73139948fdb450f407f91bb5e5719fcda6fdcbe81741ae0596b22e1a4d9`  
		Last Modified: Sat, 01 Jun 2024 01:48:47 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e0f5e07de301adaed1e01154d47eaa5c187ff12d66fed797fbbf55d023c61`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5382104801e34c28ad905e53274ba42e826eb477001c2c5ab8c387f12b8034`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51e33d390c47683332802f3f782c82d5d12c53a93338c10a3ef9d9c0275c0a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974510818003ea4918313a2a6fb387f51323e326a84ec342b0efc458f26654df`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25102898941994673476a3a0166417076418cc27be3d011b1d8bfd36d3956a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0de5b89a74693e7c1cafee5c10c44924b090612ed324489c4440456eca54ee8`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:2434bdc36f05dd7e07042c6fa7a720124e44be8258272413e0e1a0af5a51f06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:7ce7e1dd021e1ce821e2609d471975c2ac67ee334fe8eee6db8c0d22996f33bf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250330853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee8737267229bfb00293e2a379dfe28a1761c48600c808d4f63f3d929e43e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 01 Jun 2024 01:43:19 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:15 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:44:16 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:44:16 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:44:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:44:17 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:44:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:44:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:44:23 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:44:24 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:44:24 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 01 Jun 2024 01:44:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:44:24 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:44:24 GMT
USER 1001
# Sat, 01 Jun 2024 01:44:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849a437aa8e7437bbfe3be1495bc80750d7fdc26fd505c8ce32ceb970f53d109`  
		Last Modified: Sat, 01 Jun 2024 01:49:04 GMT  
		Size: 136.3 MB (136272862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bdb73139948fdb450f407f91bb5e5719fcda6fdcbe81741ae0596b22e1a4d9`  
		Last Modified: Sat, 01 Jun 2024 01:48:47 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e0f5e07de301adaed1e01154d47eaa5c187ff12d66fed797fbbf55d023c61`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5382104801e34c28ad905e53274ba42e826eb477001c2c5ab8c387f12b8034`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51e33d390c47683332802f3f782c82d5d12c53a93338c10a3ef9d9c0275c0a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974510818003ea4918313a2a6fb387f51323e326a84ec342b0efc458f26654df`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25102898941994673476a3a0166417076418cc27be3d011b1d8bfd36d3956a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0de5b89a74693e7c1cafee5c10c44924b090612ed324489c4440456eca54ee8`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:c0b020618a09dc45863e88b04cd73752f9c14264fc0c03d3abd3f8bf1558b446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:3e39c5a0e1ac3cd30ea72fc53b838704bf9d7c7142b689a527fb0e35ecad970c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262943048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e81e779d413b7e8ce0508054daa235ae20bcb515101ba78c5c5d8184095a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 01 Jun 2024 01:41:55 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:42:52 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:42:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:42:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:42:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:42:54 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:42:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:43:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:43:01 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:43:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:43:02 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:43:02 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:43:02 GMT
USER 1001
# Sat, 01 Jun 2024 01:43:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a97f1b5cc25edef1d5b526a423e078f6807d807e3093fa89e53d71520c5243`  
		Last Modified: Sat, 01 Jun 2024 01:48:35 GMT  
		Size: 148.9 MB (148885063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d6a1f0c59dc00478baf0d3722d7e8b878faedfcffb44eed7c444bc961eba68`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bc2875cdd31896903b89eb3c408137e935f68b6f4aab0738f5c31ea36cc36d`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2ef585751ffe86c9abf2036e79b3662f8211e45c1f8d6328a27a94aafc456`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0b7ab7f1ab43343275b195b09b2190ae4fd99811725aa5279a5fb966bbc0df`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203498c21995eebfeb5168b2efafb723daa8740d2b2b694403b72f4c0fa7ddb2`  
		Last Modified: Sat, 01 Jun 2024 01:48:16 GMT  
		Size: 8.1 MB (8137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88455981b7aea57ba97fc18d19a74382b9fd56c5a4bc7712fbc5adbf4c92279`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c34f5780bbfb18aa44954dc54dbe5b526ba14564e052d993c9800b93492a04d`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:c0b020618a09dc45863e88b04cd73752f9c14264fc0c03d3abd3f8bf1558b446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:3e39c5a0e1ac3cd30ea72fc53b838704bf9d7c7142b689a527fb0e35ecad970c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262943048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e81e779d413b7e8ce0508054daa235ae20bcb515101ba78c5c5d8184095a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 01 Jun 2024 01:41:55 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:42:52 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:42:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:42:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:42:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:42:54 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:42:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:43:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:43:01 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:43:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:43:02 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:43:02 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:43:02 GMT
USER 1001
# Sat, 01 Jun 2024 01:43:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a97f1b5cc25edef1d5b526a423e078f6807d807e3093fa89e53d71520c5243`  
		Last Modified: Sat, 01 Jun 2024 01:48:35 GMT  
		Size: 148.9 MB (148885063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d6a1f0c59dc00478baf0d3722d7e8b878faedfcffb44eed7c444bc961eba68`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bc2875cdd31896903b89eb3c408137e935f68b6f4aab0738f5c31ea36cc36d`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2ef585751ffe86c9abf2036e79b3662f8211e45c1f8d6328a27a94aafc456`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0b7ab7f1ab43343275b195b09b2190ae4fd99811725aa5279a5fb966bbc0df`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203498c21995eebfeb5168b2efafb723daa8740d2b2b694403b72f4c0fa7ddb2`  
		Last Modified: Sat, 01 Jun 2024 01:48:16 GMT  
		Size: 8.1 MB (8137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88455981b7aea57ba97fc18d19a74382b9fd56c5a4bc7712fbc5adbf4c92279`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c34f5780bbfb18aa44954dc54dbe5b526ba14564e052d993c9800b93492a04d`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:48f78ebf742a35ea55376c3cca396780c28bbacfd2ee1357f69359f08edadce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:df1a54b6cee49216889445b884a4d14d3a9a6b99b99e0d5b7b25e3d75a06cc45
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42522f485271f9748885c56323b6bc803feab43fef8e286bdbe0bbe6eacae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 01 Jun 2024 01:40:34 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:41:35 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:41:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:41:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:41:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:41:37 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:41:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:41:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:41:44 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:41:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:41:45 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:41:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:41:45 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:41:45 GMT
USER 1001
# Sat, 01 Jun 2024 01:41:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52eeebf7e9015b99a65edf866b86682b1d745a0050eeb7a476d6a24b9090f4c8`  
		Last Modified: Sat, 01 Jun 2024 01:48:06 GMT  
		Size: 172.4 MB (172397673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0c1ecc7a4744158d8a26c9107ddd591df11677a7f064f85cbd372897c85d39`  
		Last Modified: Sat, 01 Jun 2024 01:47:45 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259af95ff3d778451f2bfcb7bfcb6d62236cbaedc4b0d6413b1cac0741f0df1a`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e12b7e434a5d9eac09b03796cd6c5a8694329002efae544432a501922ef94e3`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f514f8ad82fc8266547a06e30aa7642ca6e66e06109f7b35dfdd65ac7f9646`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912e7ca9d0ddb57b2d4cbd3ab4f4b52c501e72fe990b07574df2d721f0bf5fc`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d966888f337f1f37a7c35d9703c8de57eeff6b56ab33bf2a2b458e614173b1ed`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7235e535bf5e070e7a5b7b9c630d3295196113422bb801a1ba1dd973b368a1`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:48f78ebf742a35ea55376c3cca396780c28bbacfd2ee1357f69359f08edadce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:df1a54b6cee49216889445b884a4d14d3a9a6b99b99e0d5b7b25e3d75a06cc45
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42522f485271f9748885c56323b6bc803feab43fef8e286bdbe0bbe6eacae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 01 Jun 2024 01:40:34 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:41:35 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:41:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:41:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:41:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:41:37 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:41:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:41:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:41:44 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:41:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:41:45 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:41:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:41:45 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:41:45 GMT
USER 1001
# Sat, 01 Jun 2024 01:41:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52eeebf7e9015b99a65edf866b86682b1d745a0050eeb7a476d6a24b9090f4c8`  
		Last Modified: Sat, 01 Jun 2024 01:48:06 GMT  
		Size: 172.4 MB (172397673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0c1ecc7a4744158d8a26c9107ddd591df11677a7f064f85cbd372897c85d39`  
		Last Modified: Sat, 01 Jun 2024 01:47:45 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259af95ff3d778451f2bfcb7bfcb6d62236cbaedc4b0d6413b1cac0741f0df1a`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e12b7e434a5d9eac09b03796cd6c5a8694329002efae544432a501922ef94e3`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f514f8ad82fc8266547a06e30aa7642ca6e66e06109f7b35dfdd65ac7f9646`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912e7ca9d0ddb57b2d4cbd3ab4f4b52c501e72fe990b07574df2d721f0bf5fc`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d966888f337f1f37a7c35d9703c8de57eeff6b56ab33bf2a2b458e614173b1ed`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7235e535bf5e070e7a5b7b9c630d3295196113422bb801a1ba1dd973b368a1`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
