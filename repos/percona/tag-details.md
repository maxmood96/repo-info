<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.39-30`](#percona8039-30)
-	[`percona:8.0.39-30-centos`](#percona8039-30-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.39-30`](#perconaps-8039-30)
-	[`percona:psmdb-5.0`](#perconapsmdb-50)
-	[`percona:psmdb-5.0.29`](#perconapsmdb-5029)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.19`](#perconapsmdb-6019)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.15`](#perconapsmdb-7015)

## `percona:8`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.39-30`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `percona:8.0.39-30-centos`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `percona:ps-8`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.39-30`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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

## `percona:psmdb-5.0.29`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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

## `percona:psmdb-6.0.19`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `percona:psmdb-7.0.15`

```console
$ docker pull percona@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
