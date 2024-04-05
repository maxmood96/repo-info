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
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
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
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.44-centos`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:5.7.44-centos` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
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
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
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
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:e8d34d02c74f9577c53b7da6d4c1cbe9785ea0ef845fb53319bdf2080bfa2985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:97fe24f512b3ebc1a436ecdf0dd00e24ccba3bd7c039d716d8c80d2b4960e4aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.0 MB (461958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a87486c21354ae3957c46e378e8bf18e66bdd6ab451b57b7036bb6792ce5af4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:45:28 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 05 Apr 2024 19:46:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 05 Apr 2024 19:46:09 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 05 Apr 2024 19:46:09 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:46:09 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 05 Apr 2024 19:46:10 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 05 Apr 2024 19:46:10 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 05 Apr 2024 19:46:10 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 05 Apr 2024 19:46:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 05 Apr 2024 19:46:51 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 05 Apr 2024 19:46:51 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 05 Apr 2024 19:46:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 05 Apr 2024 19:46:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 05 Apr 2024 19:46:52 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 05 Apr 2024 19:46:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:46:52 GMT
USER mysql
# Fri, 05 Apr 2024 19:46:52 GMT
EXPOSE 3306
# Fri, 05 Apr 2024 19:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d335d68df4dd96de12df66103800ebe48b63f3851d5fb2ad302dabfcc93e3e4`  
		Last Modified: Fri, 05 Apr 2024 19:52:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02f64a324902cbe553325559d2538be82c04fee63fbf0985df8d06a9018d48`  
		Last Modified: Fri, 05 Apr 2024 19:52:35 GMT  
		Size: 223.0 MB (223007916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf83bf52283211f36f67e0329cda51de11a553c7b35c8fcda9537e4df273f6`  
		Last Modified: Fri, 05 Apr 2024 19:52:42 GMT  
		Size: 138.1 MB (138143677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac16c5968453fbae7f570ec3bde26d60a134763bfc1611ddbb37145e8a724e1`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c535484dc3131c20baa3a322fa83dcea980a026548d694da1065be068190e`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 4.1 KB (4063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621ace6568fea865acd1c2ba3991e20ada14253ae65463f4eff13c15c015cad`  
		Last Modified: Fri, 05 Apr 2024 19:52:24 GMT  
		Size: 3.3 KB (3288 bytes)  
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
$ docker pull percona@sha256:4db38fb39a1a8a5bad0f541e4568b3fa04d2fb0266d8fe971d3623a87783e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:bab42bf36d1f46b791aef1f9edfc9e1e8dac2a43be21b3660eded404af3ba9ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231937861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fda1fed8ae73f0379aff1744454071ca7133ef313d69dfa9fb09773be1927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:50:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 05 Apr 2024 19:50:53 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:50:54 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:51:49 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:51:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:51:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:51:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:51:50 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:51:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:51:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:51:56 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:51:56 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:51:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:51:56 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:51:56 GMT
USER 1001
# Fri, 05 Apr 2024 19:51:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d2a44141d5dac15139bb0f28d1ce310a86fa427ed396864b7baeff18eff42f`  
		Last Modified: Fri, 05 Apr 2024 19:54:41 GMT  
		Size: 4.3 MB (4288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b644f560a7f50cdbb4e58782f763501cf0d4ef41d407a8f539a160780921d9f`  
		Last Modified: Fri, 05 Apr 2024 19:54:56 GMT  
		Size: 117.8 MB (117765835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b439ff74eea14435bf8f0d17e15be258bbcc3c498a52c5c92e829c8af9e6be9`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120df9157f96834b7d7441651f64378902cb4b3a20e2acee37db0c66df620e8a`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be04f142be47aac9fd5d13567457bfb725e43c638d7bd93866de2f2e8d2580b`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653537ce9c3c521b43f7565a55067de70fa9d874e5fe2526cb462fe86816462`  
		Last Modified: Fri, 05 Apr 2024 19:54:39 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f540454f6a1e1e8934421761cfc483c999b45dca64f23b47bd1590fe06db12f0`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5721bb3989f1595f38b277a64db2c9fcc51f291bc10277d47a29e972722b3d`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:4db38fb39a1a8a5bad0f541e4568b3fa04d2fb0266d8fe971d3623a87783e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:bab42bf36d1f46b791aef1f9edfc9e1e8dac2a43be21b3660eded404af3ba9ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231937861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fda1fed8ae73f0379aff1744454071ca7133ef313d69dfa9fb09773be1927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:50:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 05 Apr 2024 19:50:53 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:50:54 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:51:49 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:51:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:51:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:51:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:51:50 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:51:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:51:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:51:56 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:51:56 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:51:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:51:56 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:51:56 GMT
USER 1001
# Fri, 05 Apr 2024 19:51:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d2a44141d5dac15139bb0f28d1ce310a86fa427ed396864b7baeff18eff42f`  
		Last Modified: Fri, 05 Apr 2024 19:54:41 GMT  
		Size: 4.3 MB (4288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b644f560a7f50cdbb4e58782f763501cf0d4ef41d407a8f539a160780921d9f`  
		Last Modified: Fri, 05 Apr 2024 19:54:56 GMT  
		Size: 117.8 MB (117765835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b439ff74eea14435bf8f0d17e15be258bbcc3c498a52c5c92e829c8af9e6be9`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120df9157f96834b7d7441651f64378902cb4b3a20e2acee37db0c66df620e8a`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be04f142be47aac9fd5d13567457bfb725e43c638d7bd93866de2f2e8d2580b`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653537ce9c3c521b43f7565a55067de70fa9d874e5fe2526cb462fe86816462`  
		Last Modified: Fri, 05 Apr 2024 19:54:39 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f540454f6a1e1e8934421761cfc483c999b45dca64f23b47bd1590fe06db12f0`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5721bb3989f1595f38b277a64db2c9fcc51f291bc10277d47a29e972722b3d`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:65b68fd8c09b4c0304b3d7153dcc7ea1694be5e80eb37fe948e75a77ec12bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:5d90ec4cb9a5ff479db6f7ae37a653adee5d3d652e7fcbbde8c0278c417a9886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250456238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50913c5b9b3c2853ad15b363c391405648d73dabe488d2df984045596656f702`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:49:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 05 Apr 2024 19:49:43 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:49:44 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:39 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:50:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:50:41 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:50:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:50:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:50:47 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:50:48 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:50:48 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 05 Apr 2024 19:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:50:48 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:50:48 GMT
USER 1001
# Fri, 05 Apr 2024 19:50:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbbe57d18d24736c1d1b3ff6c549e10d6bd9083176765aee196dbad13fa4a8c`  
		Last Modified: Fri, 05 Apr 2024 19:54:29 GMT  
		Size: 136.3 MB (136284563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc0974382b68e21d3c497cdc6498b3bf368b5af6897e3aa0c8eb140a1aa13c4`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8844c2b540df45e7d629f89a1e6cb442ff4d578b2f676e4476424cfcfceb5a64`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9169e69a2057a8f06a53716519693658a7fcbe718e6d9619aa8d55d5b149001d`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9b7de59b007697cb9827a4e350398d3eb8b2476ebeef528c0936930b16bbf1`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65011163cb64940679b0644276e5f8fb1bf2af36d22c914668f166f20721026`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71944d9d13a6f3633f70c759812caeee4d3117a09831dae121ebb27c8d93657`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904666679d8d9fac9af37bfaf29efb6f9b249557ddfbbfc45061cb3a13829011`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:65b68fd8c09b4c0304b3d7153dcc7ea1694be5e80eb37fe948e75a77ec12bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:5d90ec4cb9a5ff479db6f7ae37a653adee5d3d652e7fcbbde8c0278c417a9886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250456238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50913c5b9b3c2853ad15b363c391405648d73dabe488d2df984045596656f702`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:49:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 05 Apr 2024 19:49:43 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:49:44 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:39 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:50:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:50:41 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:50:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:50:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:50:47 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:50:48 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:50:48 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 05 Apr 2024 19:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:50:48 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:50:48 GMT
USER 1001
# Fri, 05 Apr 2024 19:50:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbbe57d18d24736c1d1b3ff6c549e10d6bd9083176765aee196dbad13fa4a8c`  
		Last Modified: Fri, 05 Apr 2024 19:54:29 GMT  
		Size: 136.3 MB (136284563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc0974382b68e21d3c497cdc6498b3bf368b5af6897e3aa0c8eb140a1aa13c4`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8844c2b540df45e7d629f89a1e6cb442ff4d578b2f676e4476424cfcfceb5a64`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9169e69a2057a8f06a53716519693658a7fcbe718e6d9619aa8d55d5b149001d`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9b7de59b007697cb9827a4e350398d3eb8b2476ebeef528c0936930b16bbf1`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65011163cb64940679b0644276e5f8fb1bf2af36d22c914668f166f20721026`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71944d9d13a6f3633f70c759812caeee4d3117a09831dae121ebb27c8d93657`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904666679d8d9fac9af37bfaf29efb6f9b249557ddfbbfc45061cb3a13829011`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:38757ba32542991d0e39e9d6ff24fbda29e51f230f324678501487787b36bdf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:5f297468279b297be9f85b744865d3b9c0c7ed310518423d4690e3fa4bdf2828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263074402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227e545ad8b2f3a48f9b4f7cce0858dd77277a227bc4565a6da5d58941b62105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 05 Apr 2024 19:48:33 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:49:29 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:49:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:49:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:49:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:49:31 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:49:34 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:49:36 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:49:37 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:49:37 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:49:37 GMT
USER 1001
# Fri, 05 Apr 2024 19:49:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc1c5a5d8764f1bae0e6f9cb85623ad7d7dc5dc86f7c362363a0eec133a960`  
		Last Modified: Fri, 05 Apr 2024 19:54:00 GMT  
		Size: 148.9 MB (148902725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc280794bd1d369744e8fdc4e159b80cbee5c6834b8e79b0c89fa5b90cf1da86`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b53458941f4cfbc5e3cfaa1bbbc48e3650f4f80da3e2659045e814d1d46c63b`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b6833b960d7b4ca7de8e5635a96183fd3d23f599e6ff177b99324eb14174a0`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74451a5de30ed5ea18d21fecfeaed975e141fdeee092765dfb49905aeaf0eb1a`  
		Last Modified: Fri, 05 Apr 2024 19:53:41 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a2759586cac3dc57d8ab09e45b8c50a26374d51d1d041fbe5f0061dcfceb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02922457eb36f02de272c19413fbb3acf907396c713ae7ac647cbe35f3d3182b`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd67c841a9e9e53ccd428bdefaa4fedc10e5605d630ed8d53aec23a313f513f`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:38757ba32542991d0e39e9d6ff24fbda29e51f230f324678501487787b36bdf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:5f297468279b297be9f85b744865d3b9c0c7ed310518423d4690e3fa4bdf2828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263074402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227e545ad8b2f3a48f9b4f7cce0858dd77277a227bc4565a6da5d58941b62105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 05 Apr 2024 19:48:33 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:49:29 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:49:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:49:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:49:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:49:31 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:49:34 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:49:36 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:49:37 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:49:37 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:49:37 GMT
USER 1001
# Fri, 05 Apr 2024 19:49:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc1c5a5d8764f1bae0e6f9cb85623ad7d7dc5dc86f7c362363a0eec133a960`  
		Last Modified: Fri, 05 Apr 2024 19:54:00 GMT  
		Size: 148.9 MB (148902725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc280794bd1d369744e8fdc4e159b80cbee5c6834b8e79b0c89fa5b90cf1da86`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b53458941f4cfbc5e3cfaa1bbbc48e3650f4f80da3e2659045e814d1d46c63b`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b6833b960d7b4ca7de8e5635a96183fd3d23f599e6ff177b99324eb14174a0`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74451a5de30ed5ea18d21fecfeaed975e141fdeee092765dfb49905aeaf0eb1a`  
		Last Modified: Fri, 05 Apr 2024 19:53:41 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a2759586cac3dc57d8ab09e45b8c50a26374d51d1d041fbe5f0061dcfceb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02922457eb36f02de272c19413fbb3acf907396c713ae7ac647cbe35f3d3182b`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd67c841a9e9e53ccd428bdefaa4fedc10e5605d630ed8d53aec23a313f513f`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:7ee35c22a4f74094efc8a1014783775aea7a0f878a83cc6cf309eb7bb7163fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:c2fb8ef4602ef2957640cb4e695028b0faa76b8735897be208a279176fca1b07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286582022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5989663c1e0a04b170ed9632f2a329cfea68264d2f172e351ec726fbae49fdb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 05 Apr 2024 19:47:12 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:48:10 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:48:12 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:48:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:48:12 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:48:12 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:48:16 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:48:18 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:48:18 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:48:19 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:48:19 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:48:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:48:19 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:48:19 GMT
USER 1001
# Fri, 05 Apr 2024 19:48:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57d6b900a2e3a585db270fcac060ff18db5bb94a6c938929afbf6fbc8bfb10`  
		Last Modified: Fri, 05 Apr 2024 19:53:31 GMT  
		Size: 172.4 MB (172410341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9963581396707030b08191494a0cd99c207fbd7d74590d38d2c1ffd6c79300eb`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0ca7a3502a73fc6a9ad02214e7862ed3484a5891272781c294ec4bb7eac607`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc684023ab7b463fa333d090d63fc6ce1712c2543c739dc0bacbebac2633ccb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3414366b648845db803a466b87071b3ffb88dc75790d5eab673b874c06b343c`  
		Last Modified: Fri, 05 Apr 2024 19:53:09 GMT  
		Size: 914.5 KB (914546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3871d1502b7043994f20a5131576ef297a05343a7133be13d1ee433ee8e0b`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d4f1a856538f872e9ec92a01afc05d852385b6bc9016a32bba014c04d39254`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2fa33e5ccc4ab803503963ad17beaf34eb4d24bda17f7354ca339337c21dde`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:7ee35c22a4f74094efc8a1014783775aea7a0f878a83cc6cf309eb7bb7163fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:c2fb8ef4602ef2957640cb4e695028b0faa76b8735897be208a279176fca1b07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286582022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5989663c1e0a04b170ed9632f2a329cfea68264d2f172e351ec726fbae49fdb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 05 Apr 2024 19:47:12 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:48:10 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:48:12 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:48:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:48:12 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:48:12 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:48:16 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:48:18 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:48:18 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:48:19 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:48:19 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:48:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:48:19 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:48:19 GMT
USER 1001
# Fri, 05 Apr 2024 19:48:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57d6b900a2e3a585db270fcac060ff18db5bb94a6c938929afbf6fbc8bfb10`  
		Last Modified: Fri, 05 Apr 2024 19:53:31 GMT  
		Size: 172.4 MB (172410341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9963581396707030b08191494a0cd99c207fbd7d74590d38d2c1ffd6c79300eb`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0ca7a3502a73fc6a9ad02214e7862ed3484a5891272781c294ec4bb7eac607`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc684023ab7b463fa333d090d63fc6ce1712c2543c739dc0bacbebac2633ccb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3414366b648845db803a466b87071b3ffb88dc75790d5eab673b874c06b343c`  
		Last Modified: Fri, 05 Apr 2024 19:53:09 GMT  
		Size: 914.5 KB (914546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3871d1502b7043994f20a5131576ef297a05343a7133be13d1ee433ee8e0b`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d4f1a856538f872e9ec92a01afc05d852385b6bc9016a32bba014c04d39254`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2fa33e5ccc4ab803503963ad17beaf34eb4d24bda17f7354ca339337c21dde`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
