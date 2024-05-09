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
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
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
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.36-28-centos`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0.36-28-centos` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
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
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.36-28`

```console
$ docker pull percona@sha256:4cbaf1b6c054f2a1148eb56daf7321e68c444c231248bcaf12ba86d435255373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:a939733eaf525c343b6c004a0159c73bed1207b01ee60248b76d1f0fe2bded9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba824cf3ae1b623c33a760a93aea3b025d0bf174e2eafbb668a7ba4a8bb504ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:03 GMT
ADD file:d758a1b66f956f0cc3e96041f5c36a48a243646ea0f1ac744729eb7b77310a4d in / 
# Thu, 09 May 2024 22:30:04 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:48:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:48:23 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 09 May 2024 22:48:23 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 09 May 2024 22:48:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 09 May 2024 22:48:24 GMT
ENV OS_VER=el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_REPO=release
# Thu, 09 May 2024 22:48:24 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:48:24 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:48:24 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:48:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 09 May 2024 22:49:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:49:41 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 09 May 2024 22:49:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:49:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:49:43 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 09 May 2024 22:49:43 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:49:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:49:43 GMT
USER mysql
# Thu, 09 May 2024 22:49:43 GMT
EXPOSE 3306 33060
# Thu, 09 May 2024 22:49:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:746c723f6b7fd7903e265d130424d7a2940a2335d0d3198f914469d7fb671163`  
		Last Modified: Thu, 09 May 2024 22:31:39 GMT  
		Size: 95.5 MB (95453739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f936476787e7bfe73411c7254760ef5826b7f6ffe7365afcec0dfde469d9e`  
		Last Modified: Thu, 09 May 2024 22:56:44 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83474d5709c5aa7d46d7969c68251b4b2fe72becde1453b378af840f50483c`  
		Last Modified: Thu, 09 May 2024 22:56:43 GMT  
		Size: 7.3 MB (7323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649624e55dd7b2eb42b8084fac3998ad3fe071a9b57c5e41c36ff13dc17347c`  
		Last Modified: Thu, 09 May 2024 22:57:24 GMT  
		Size: 296.0 MB (296040011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb501ce5bbf94cb2418e91496c4e9c0cb4cf43181e82fa80cbac577ad4513cb4`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce318fdde946c817eedb4d5333999d666523709f29b2382999784914f138eaf`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8858f8a68ba3af7ec61a0ed6d1db74582a5388fa4ff73529b886247a67425489`  
		Last Modified: Thu, 09 May 2024 22:56:42 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:eed45e763eccb11c906de62f0a943bc809133d88070e9069e6fb3e494bf1d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:f95c44107b43b992435b52822db2c7b37217a4ea69f0e57da4bfd436364ba69a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231959783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2664a5c02c25e8805c42e6e52558713dfaf07c3c765b9f53fd8278a23cedcd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:55:12 GMT
ENV PSMDB_VERSION=4.2.24-24
# Thu, 09 May 2024 22:55:12 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:55:12 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Thu, 09 May 2024 22:55:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:55:12 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:55:15 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:56:08 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:56:09 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:56:10 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:56:10 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:56:10 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:56:13 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:56:15 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:56:16 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:56:16 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 09 May 2024 22:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:56:16 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:56:16 GMT
USER 1001
# Thu, 09 May 2024 22:56:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e633972f8faa73eb2a45011b8c8c1811a3d1b47c51c70e424f8dd1708e264`  
		Last Modified: Thu, 09 May 2024 23:00:03 GMT  
		Size: 4.3 MB (4297846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d9ffc6f516f7a70ac5c1c862f90614f84ab712bd5909f053894821ebe1104`  
		Last Modified: Thu, 09 May 2024 23:00:17 GMT  
		Size: 117.8 MB (117773972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8cfd97cf36a20e7512dbe4bd66b8f01a681549272da68d557fedc62fb5306`  
		Last Modified: Thu, 09 May 2024 23:00:02 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0007eec4f3f7caca10edbbd6297d6b771f5c24bb4e1c63a8379a8481ce4633`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf883b36e162be9dad19097f0e22676a5a954b9d503d855fc53079e1df2a311a`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f880b3ce91a96cde9788ad9b2e95e9f7c5f3bc877ba74c4c3c813eb7c282a4b`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c0730a814c673326ecd231ec8076ef848f200133d9b680509cabbc74000e4d`  
		Last Modified: Thu, 09 May 2024 23:00:01 GMT  
		Size: 8.2 MB (8151459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5021e1eba177c583f7a94de44c0830ea6d5df21cb56e576f8e9964c5c54f57`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:eed45e763eccb11c906de62f0a943bc809133d88070e9069e6fb3e494bf1d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:f95c44107b43b992435b52822db2c7b37217a4ea69f0e57da4bfd436364ba69a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231959783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2664a5c02c25e8805c42e6e52558713dfaf07c3c765b9f53fd8278a23cedcd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:55:12 GMT
ENV PSMDB_VERSION=4.2.24-24
# Thu, 09 May 2024 22:55:12 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:55:12 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Thu, 09 May 2024 22:55:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:55:12 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:55:15 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:56:08 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:56:09 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:56:10 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:56:10 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:56:10 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:56:13 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:56:15 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:56:16 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:56:16 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 09 May 2024 22:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:56:16 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:56:16 GMT
USER 1001
# Thu, 09 May 2024 22:56:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e633972f8faa73eb2a45011b8c8c1811a3d1b47c51c70e424f8dd1708e264`  
		Last Modified: Thu, 09 May 2024 23:00:03 GMT  
		Size: 4.3 MB (4297846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d9ffc6f516f7a70ac5c1c862f90614f84ab712bd5909f053894821ebe1104`  
		Last Modified: Thu, 09 May 2024 23:00:17 GMT  
		Size: 117.8 MB (117773972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8cfd97cf36a20e7512dbe4bd66b8f01a681549272da68d557fedc62fb5306`  
		Last Modified: Thu, 09 May 2024 23:00:02 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0007eec4f3f7caca10edbbd6297d6b771f5c24bb4e1c63a8379a8481ce4633`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf883b36e162be9dad19097f0e22676a5a954b9d503d855fc53079e1df2a311a`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f880b3ce91a96cde9788ad9b2e95e9f7c5f3bc877ba74c4c3c813eb7c282a4b`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c0730a814c673326ecd231ec8076ef848f200133d9b680509cabbc74000e4d`  
		Last Modified: Thu, 09 May 2024 23:00:01 GMT  
		Size: 8.2 MB (8151459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5021e1eba177c583f7a94de44c0830ea6d5df21cb56e576f8e9964c5c54f57`  
		Last Modified: Thu, 09 May 2024 23:00:00 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:58e974022f9db146f393f96158fcdcb836dd7da0def4f7bb200b5105cfb752c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:083b66c833f5f8fc6f0545cb41f3a022ea3dfc594eee9d22a9484072b4d7827a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fe88730a3b801d4007b22353e30426ecb7ce1cf8a6e048f72d559f377747ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_VERSION=4.4.22-21
# Thu, 09 May 2024 22:54:02 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:54:02 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Thu, 09 May 2024 22:54:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:54:57 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:54:59 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:54:59 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:54:59 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:54:59 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:55:03 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:55:05 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:55:05 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:55:06 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:55:06 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 09 May 2024 22:55:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:55:06 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:55:06 GMT
USER 1001
# Thu, 09 May 2024 22:55:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c82957f5bf3dce34bc5417475d631942a90f102663b0ba8817e504ddf51b6ff`  
		Last Modified: Thu, 09 May 2024 22:59:52 GMT  
		Size: 136.3 MB (136292717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7016c000e84294a551da31987b817606cb5f842270211d476050247e0daba9`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90797bb93bf59f01c0639d3fd340645cb9691af9683a9702dca20e1f51999576`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49fa6f27b0c9be0455889d39273c15a0ffa83fa0b198f35b7dedbf80ee87e05`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77b145c0af7f6c252d5e3680e15463d0ba269dc297413dc71e2362ccb37908`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb52ba09da7b6a9553017e86edcf51e038bf72b799cdc9765f8abac605e379d5`  
		Last Modified: Thu, 09 May 2024 22:59:34 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac9781b18e161913e927fe5a6546829dc3fb0b2a8fa331332778bfb2d79c86`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca3476fe08bc6c190e3fa0d40028966ae476e6dde9698df6c3d6ace841d19ff`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:58e974022f9db146f393f96158fcdcb836dd7da0def4f7bb200b5105cfb752c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:083b66c833f5f8fc6f0545cb41f3a022ea3dfc594eee9d22a9484072b4d7827a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fe88730a3b801d4007b22353e30426ecb7ce1cf8a6e048f72d559f377747ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_VERSION=4.4.22-21
# Thu, 09 May 2024 22:54:02 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:54:02 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Thu, 09 May 2024 22:54:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:54:57 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:54:59 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:54:59 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:54:59 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:54:59 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:55:03 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:55:05 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:55:05 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:55:06 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:55:06 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 09 May 2024 22:55:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:55:06 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:55:06 GMT
USER 1001
# Thu, 09 May 2024 22:55:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c82957f5bf3dce34bc5417475d631942a90f102663b0ba8817e504ddf51b6ff`  
		Last Modified: Thu, 09 May 2024 22:59:52 GMT  
		Size: 136.3 MB (136292717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7016c000e84294a551da31987b817606cb5f842270211d476050247e0daba9`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90797bb93bf59f01c0639d3fd340645cb9691af9683a9702dca20e1f51999576`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49fa6f27b0c9be0455889d39273c15a0ffa83fa0b198f35b7dedbf80ee87e05`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77b145c0af7f6c252d5e3680e15463d0ba269dc297413dc71e2362ccb37908`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb52ba09da7b6a9553017e86edcf51e038bf72b799cdc9765f8abac605e379d5`  
		Last Modified: Thu, 09 May 2024 22:59:34 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac9781b18e161913e927fe5a6546829dc3fb0b2a8fa331332778bfb2d79c86`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca3476fe08bc6c190e3fa0d40028966ae476e6dde9698df6c3d6ace841d19ff`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:f641c2d3628038fb33a89986376790ab9fb95f84f81c54ac61c726c5befaf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:b0010065796bf22a39650185d5147047e3e5834bc502cacb3b98a98c24404366
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263081395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706626b126c5ac852e69f15fcaed42052462300520072d73995d72c9aa5bfd38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_VERSION=5.0.18-15
# Thu, 09 May 2024 22:52:52 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:52:52 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Thu, 09 May 2024 22:52:52 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:53:48 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:53:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:53:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:53:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:53:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:53:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:53:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:53:55 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:53:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:53:56 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 09 May 2024 22:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:53:56 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:53:56 GMT
USER 1001
# Thu, 09 May 2024 22:53:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211782ad7d02bd0eeee8cf9091490ca4f1d54205f32a95ce11f2bcf07f6b64f`  
		Last Modified: Thu, 09 May 2024 22:59:24 GMT  
		Size: 148.9 MB (148895973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f835a8bc63440967b9cb11598ff2cc53653d0b792385c4bc00cb0abd24fbddfd`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727aea791b52fbb3fef4ee0fcfef4c9cd446278ab7ed0893aec30e882f11ccd4`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5177a5fe558b8b0510657aa7aff0f63b994a807103c2b8c8ff830bcdce14c314`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d1a14cf48c9cf9d2811791256b547d194e4464e7df8b437a442c784f073883`  
		Last Modified: Thu, 09 May 2024 22:59:05 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb257e3773ad4746dd279d5e968c36b0b14158d57c43f25875e56255317408`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ead6839765afb0c5e7cabcad29242c6fa190e6856b0d7042a3472b3090009d6`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fdd9a787aa0a5d128a2e88246c7fb5ab158b65abf1fd859d5a39eec5d146f`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:f641c2d3628038fb33a89986376790ab9fb95f84f81c54ac61c726c5befaf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:b0010065796bf22a39650185d5147047e3e5834bc502cacb3b98a98c24404366
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263081395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706626b126c5ac852e69f15fcaed42052462300520072d73995d72c9aa5bfd38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_VERSION=5.0.18-15
# Thu, 09 May 2024 22:52:52 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:52:52 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Thu, 09 May 2024 22:52:52 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:53:48 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:53:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:53:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:53:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:53:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:53:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:53:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:53:55 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:53:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:53:56 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 09 May 2024 22:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:53:56 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:53:56 GMT
USER 1001
# Thu, 09 May 2024 22:53:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211782ad7d02bd0eeee8cf9091490ca4f1d54205f32a95ce11f2bcf07f6b64f`  
		Last Modified: Thu, 09 May 2024 22:59:24 GMT  
		Size: 148.9 MB (148895973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f835a8bc63440967b9cb11598ff2cc53653d0b792385c4bc00cb0abd24fbddfd`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727aea791b52fbb3fef4ee0fcfef4c9cd446278ab7ed0893aec30e882f11ccd4`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5177a5fe558b8b0510657aa7aff0f63b994a807103c2b8c8ff830bcdce14c314`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d1a14cf48c9cf9d2811791256b547d194e4464e7df8b437a442c784f073883`  
		Last Modified: Thu, 09 May 2024 22:59:05 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb257e3773ad4746dd279d5e968c36b0b14158d57c43f25875e56255317408`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ead6839765afb0c5e7cabcad29242c6fa190e6856b0d7042a3472b3090009d6`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fdd9a787aa0a5d128a2e88246c7fb5ab158b65abf1fd859d5a39eec5d146f`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:05c2a1caf82b474f3dcc697e2317409e14ba612e45788156636e7e10be57c1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:dc001f31db6818d852a65dacbb6250493674eb12f47e026c0ae4a50edf57c806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286600500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79a2b60cb90cd555517b053e154423f80c3d08ebdc0d2afb271b0586ccc2bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:51:30 GMT
ENV PSMDB_VERSION=6.0.6-5
# Thu, 09 May 2024 22:51:31 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:51:31 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Thu, 09 May 2024 22:51:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:51:31 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:52:29 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:52:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:52:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:52:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:52:31 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:52:35 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:52:38 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:52:38 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:52:39 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:52:39 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Thu, 09 May 2024 22:52:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:52:39 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:52:39 GMT
USER 1001
# Thu, 09 May 2024 22:52:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee38ae1140e3a8828df989148fcfb98409d849be391a106b2aed0fac581ee404`  
		Last Modified: Thu, 09 May 2024 22:58:56 GMT  
		Size: 172.4 MB (172415073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532fe1d446fddb9af95a42bfa54208e496835cf7a1bfef3967f791c2b21fd4ee`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc4651397bb268cdb31c68945c59e40c3cd1b3d9951acdf57c113c3b15ec63`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd05da12b796b9676cb4bc9aa4819de3860959f35cbd3fe3ebe4022a40f00ae3`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cca77b93916e911255dba27fac117176a2eff9c5237436b9458f2f6ed5661f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d7ec866d8a821d8ec4ce4029e7fc24ee2bab43b7064d31c89686bc38065bf6`  
		Last Modified: Thu, 09 May 2024 22:58:34 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb579de012d104163b595e489034b01d55bcb8eba4cff1d4bc1f2e9d4d5170f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf034b1c380971aea65ca491269139a78cce4fbb189e1b683f67a4f8c8b599c`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:05c2a1caf82b474f3dcc697e2317409e14ba612e45788156636e7e10be57c1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:dc001f31db6818d852a65dacbb6250493674eb12f47e026c0ae4a50edf57c806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286600500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79a2b60cb90cd555517b053e154423f80c3d08ebdc0d2afb271b0586ccc2bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:51:30 GMT
ENV PSMDB_VERSION=6.0.6-5
# Thu, 09 May 2024 22:51:31 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:51:31 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Thu, 09 May 2024 22:51:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:51:31 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:52:29 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:52:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:52:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:52:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:52:31 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:52:35 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:52:38 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:52:38 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:52:39 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:52:39 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Thu, 09 May 2024 22:52:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:52:39 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:52:39 GMT
USER 1001
# Thu, 09 May 2024 22:52:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee38ae1140e3a8828df989148fcfb98409d849be391a106b2aed0fac581ee404`  
		Last Modified: Thu, 09 May 2024 22:58:56 GMT  
		Size: 172.4 MB (172415073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532fe1d446fddb9af95a42bfa54208e496835cf7a1bfef3967f791c2b21fd4ee`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc4651397bb268cdb31c68945c59e40c3cd1b3d9951acdf57c113c3b15ec63`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd05da12b796b9676cb4bc9aa4819de3860959f35cbd3fe3ebe4022a40f00ae3`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cca77b93916e911255dba27fac117176a2eff9c5237436b9458f2f6ed5661f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d7ec866d8a821d8ec4ce4029e7fc24ee2bab43b7064d31c89686bc38065bf6`  
		Last Modified: Thu, 09 May 2024 22:58:34 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb579de012d104163b595e489034b01d55bcb8eba4cff1d4bc1f2e9d4d5170f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf034b1c380971aea65ca491269139a78cce4fbb189e1b683f67a4f8c8b599c`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
