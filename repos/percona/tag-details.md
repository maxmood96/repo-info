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
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.39-30`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.39-30` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.39-30` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.39-30-centos`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.39-30-centos` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.39-30-centos` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.39-30`

```console
$ docker pull percona@sha256:2446b3626ee8738d5e852e1994f204c0536952492b1f3c991f92c023303911c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.39-30` - linux; amd64

```console
$ docker pull percona@sha256:4be620559a55bd70c3bbc57ce958a9b6ff1d7050b646b6149b227c4b4a3aa7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48790fda772c34bafa52cb7869da57c7ac9218dfdff8b542c1f1699c9d72f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_VERSION=8.0.39-30.1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=8.0.39-30.1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_REPO=testing
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PS_TELEMETRY_VERSION=8.0.39-30-1
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO} # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
USER mysql
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa65e7a4e79ce88e33d3670bba8ebe9e5cc2aac0934c80ace8637bb97f839006`  
		Last Modified: Fri, 20 Dec 2024 21:29:05 GMT  
		Size: 105.5 MB (105510489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d5272be7d90e8b95ad276ec53ec6d53322aa269067a2cb3163404022017`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9bc72e820d58b41b864c4e33ffcd4537e33ee11e8e3e14ec4997b412a49de`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 8.0 MB (8020189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a33605cbffd296c71376002da5186465956bd5211de5dda93c2423e75e1cc`  
		Last Modified: Fri, 20 Dec 2024 22:31:23 GMT  
		Size: 317.3 MB (317338976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690850c621a89e6d7c4c5b01c1248bda15a144013523c2cfeb05bfa1e32e897`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798017bc5552a01f8fe5652d599f75e00362ff94ac2f57e199d71e9c9c17f0e`  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca929b08eef0c14f696ed882fa4a9cc28f103f452bdea6e3b9655166e33e52d`  
		Last Modified: Fri, 20 Dec 2024 22:31:19 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.39-30` - unknown; unknown

```console
$ docker pull percona@sha256:463aa913e3678285664b348b66b39117089885e6063a405aa3ead79a4a592688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 KB (28644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2791f4517c9652e399198c6f6e7be6692513d1bef9e6554d2a66d1c2f20c762`

```dockerfile
```

-	Layers:
	-	`sha256:6ccee53d38ea6327b4cf49fac526c410e87a3e2099e27ac8d5f6f9dae587c122`  
		Last Modified: Fri, 20 Dec 2024 22:31:18 GMT  
		Size: 28.6 KB (28644 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:8dfda2b21362bc4811611e125a55571dff0155377a599bd59dcc34938863baa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:c319c2206fdea14f7efa804050ec5ec62a0e33f4b5b18cf6b5a2beda624dadea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259716284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aad62ad78b40a2d661eabf6c68041a65d490644d8c8dff7a9a77ad73e50202`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=5.0.29-25
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=5.0.29-25.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e27459151260a9bf87af5b142b57fe29073e775d4f537455bbf42ff79c600b`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 4.3 MB (4300295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42db31b3bb6ae8d18cba110f2b5cd3d2fbf184e253024e9fad6cc96483f760e`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 153.7 MB (153686057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eec965d0f99268d7e736155ab9672ce990e5219557e516648d122490e36a086`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85ca6466fea7ec0ed541325589a9af37e82f4b05b3105f9dbc52cff7d036d55`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e4fec943efb2f88f46ac0028d2e8f8b0c3b0b8bae5cf3a009fe9b74a9b64`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012ca0f1f7ddf3049dc35d917db9cf7ac6ff8d273fb8888b1294361d90e0a5ee`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d200aed9ea80be3dab7286cc89dc37d2cae28266c40d2d127e092b0c82f935`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a63c9529cd058f8349f0d13d4e17f2e4e9f63c6f8f1153202b7b40ec3e5d2`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f6349c2343665c969270215e9deb517fce9c422e3e52b8c360c95656ed8ac3`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-5.0` - unknown; unknown

```console
$ docker pull percona@sha256:17e33dab109a4c53c590963f6d2e1feba7cfe9f4dbed6866034bbe75dfcd1c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e5ae8e3ea1a234eb4d522c7c90bbe1b9ae616b2dc58cf75930191a1ab51df0`

```dockerfile
```

-	Layers:
	-	`sha256:d62db4fa3db9ecfd18e12756bdcb6a58f51fb67732351d4ad1dad411776c9294`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 32.2 KB (32189 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-5.0.29`

```console
$ docker pull percona@sha256:8dfda2b21362bc4811611e125a55571dff0155377a599bd59dcc34938863baa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-5.0.29` - linux; amd64

```console
$ docker pull percona@sha256:c319c2206fdea14f7efa804050ec5ec62a0e33f4b5b18cf6b5a2beda624dadea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259716284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aad62ad78b40a2d661eabf6c68041a65d490644d8c8dff7a9a77ad73e50202`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=5.0.29-25
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=5.0.29-25.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e27459151260a9bf87af5b142b57fe29073e775d4f537455bbf42ff79c600b`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 4.3 MB (4300295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42db31b3bb6ae8d18cba110f2b5cd3d2fbf184e253024e9fad6cc96483f760e`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 153.7 MB (153686057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eec965d0f99268d7e736155ab9672ce990e5219557e516648d122490e36a086`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85ca6466fea7ec0ed541325589a9af37e82f4b05b3105f9dbc52cff7d036d55`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e4fec943efb2f88f46ac0028d2e8f8b0c3b0b8bae5cf3a009fe9b74a9b64`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012ca0f1f7ddf3049dc35d917db9cf7ac6ff8d273fb8888b1294361d90e0a5ee`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d200aed9ea80be3dab7286cc89dc37d2cae28266c40d2d127e092b0c82f935`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a63c9529cd058f8349f0d13d4e17f2e4e9f63c6f8f1153202b7b40ec3e5d2`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f6349c2343665c969270215e9deb517fce9c422e3e52b8c360c95656ed8ac3`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-5.0.29` - unknown; unknown

```console
$ docker pull percona@sha256:17e33dab109a4c53c590963f6d2e1feba7cfe9f4dbed6866034bbe75dfcd1c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e5ae8e3ea1a234eb4d522c7c90bbe1b9ae616b2dc58cf75930191a1ab51df0`

```dockerfile
```

-	Layers:
	-	`sha256:d62db4fa3db9ecfd18e12756bdcb6a58f51fb67732351d4ad1dad411776c9294`  
		Last Modified: Fri, 20 Dec 2024 21:29:50 GMT  
		Size: 32.2 KB (32189 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:f1d2fabf8e89f45d035dbe9becdc48c19216fc5228a9cf9835f2bcf0a886ffe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:973d4a9637ed3461356259f1b64238f21d5846da70eaa30cebcf87e0341846a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295113357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0b8e3b415ca89bb2852608158647a844fa117aff331bc2c9e50901f11606f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=6.0.19-16
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=6.0.19-16.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed10a7c65c3668320bc9569c464e5476aa869e50f6acbbff966495bfd80656`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.3 MB (4300287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1f525c5952daae690fe97a56ee94521afc7ed3b973fdbb62a4adb79d2375cf`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 189.1 MB (189083129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fd26565b10f7071e9646ed0c01527f3b2ffb298375cc2c229d34ad8a2cac5`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3aee438dc3e71e8c2094ac74be177f64afd038ee1e563e1e075ec937d888c8`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e4fec943efb2f88f46ac0028d2e8f8b0c3b0b8bae5cf3a009fe9b74a9b64`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb862443642d7f877c8aac2cf91b2edd59fd6ce92cf4b0987befb6f1213bee`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d25e61c119f3fa3c7aa25285de408851d34d20013cced88b80b69def9fa924`  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9aaa8b44ef52a2c51e6822dbf1a238ed11685e6bce31a078a0c4d52d19dd2`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5162dfce43b766555829c1240bf47376045efd134569ec9e8b2fdb347a6824`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 4.8 KB (4834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:cd8b8a042d8c1751b40ac0729ba18458c9c32942316ba63c9dc1d2fab480b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c499eabbf4d29115e4bf9c683fadb62e765ea7cc95c83c8f35e88d5e09635`

```dockerfile
```

-	Layers:
	-	`sha256:12c7973b554c20191044f6681aabd61fb430fbe6854418d59f714adefc6a67c7`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.19`

```console
$ docker pull percona@sha256:f1d2fabf8e89f45d035dbe9becdc48c19216fc5228a9cf9835f2bcf0a886ffe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.19` - linux; amd64

```console
$ docker pull percona@sha256:973d4a9637ed3461356259f1b64238f21d5846da70eaa30cebcf87e0341846a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295113357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0b8e3b415ca89bb2852608158647a844fa117aff331bc2c9e50901f11606f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=6.0.19-16
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=6.0.19-16.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed10a7c65c3668320bc9569c464e5476aa869e50f6acbbff966495bfd80656`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.3 MB (4300287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1f525c5952daae690fe97a56ee94521afc7ed3b973fdbb62a4adb79d2375cf`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 189.1 MB (189083129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fd26565b10f7071e9646ed0c01527f3b2ffb298375cc2c229d34ad8a2cac5`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3aee438dc3e71e8c2094ac74be177f64afd038ee1e563e1e075ec937d888c8`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e4fec943efb2f88f46ac0028d2e8f8b0c3b0b8bae5cf3a009fe9b74a9b64`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb862443642d7f877c8aac2cf91b2edd59fd6ce92cf4b0987befb6f1213bee`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d25e61c119f3fa3c7aa25285de408851d34d20013cced88b80b69def9fa924`  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9aaa8b44ef52a2c51e6822dbf1a238ed11685e6bce31a078a0c4d52d19dd2`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5162dfce43b766555829c1240bf47376045efd134569ec9e8b2fdb347a6824`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 4.8 KB (4834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.19` - unknown; unknown

```console
$ docker pull percona@sha256:cd8b8a042d8c1751b40ac0729ba18458c9c32942316ba63c9dc1d2fab480b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c499eabbf4d29115e4bf9c683fadb62e765ea7cc95c83c8f35e88d5e09635`

```dockerfile
```

-	Layers:
	-	`sha256:12c7973b554c20191044f6681aabd61fb430fbe6854418d59f714adefc6a67c7`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:312bf3d2b5b97e54a62083b70d9c6de2c1d671c41b37fdbe5c318a398a864e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:a03037e6a43890bfbadfeeeda0370d356902dcd4f057776146277c20a83c9e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306593320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139665776f79ed83263df8b3a58674686a05ac7049c9e263c055852d16b26486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=7.0.15-9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=7.0.15-9.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec77b46e44c57b77c9e7308150d82a4cf09cd3782e389a96b72ed9a09d6e8002`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.3 MB (4300326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d13ef4ab459ed56775ec1cf5ac74d3d5f3f899612bbc2dd628beaf590fb36`  
		Size: 200.6 MB (200563055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d0b8121c5cc316d557aeb423992506aa884f60e67337c1e59595355479cb3b`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6494bd74d14cd370421d14267513ef65c51d66d4eb787fa6c862a897043fb108`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47dad8fcc5ae5f475a141387a297bce968218f03e7bcf8987c46b184975120d`  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37854ca880477cc503f17afbec224aec2895a7012a1ce543f9132fac3ad1653`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458215f49b0524389dce9bed7edbef9f9ecbce60988a00c4057200dbb7e379de`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81896b577631381e3f353e8c7cf650af4d7ea728dfe38ce06a53e1bc779c4790`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec2793466c2f7f7bbaa6e618faf0f8d08976e845a2d4156525cde1f4d7a1a91`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.8 KB (4835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:47bf802d03a6547a6c21811f036c010d4b62a099222201b0f67c3b2c67576298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58b6c0dc95e521a3ebc3ad45e341f1e54a76229061428693ece8921fa8ac481`

```dockerfile
```

-	Layers:
	-	`sha256:c1e16bbf53cd9c84ba6e98595b1ea84a36649ab0bca620fa91910f4481dcc841`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 32.2 KB (32214 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.15`

```console
$ docker pull percona@sha256:312bf3d2b5b97e54a62083b70d9c6de2c1d671c41b37fdbe5c318a398a864e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.15` - linux; amd64

```console
$ docker pull percona@sha256:a03037e6a43890bfbadfeeeda0370d356902dcd4f057776146277c20a83c9e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306593320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139665776f79ed83263df8b3a58674686a05ac7049c9e263c055852d16b26486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=7.0.15-9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=7.0.15-9.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec77b46e44c57b77c9e7308150d82a4cf09cd3782e389a96b72ed9a09d6e8002`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.3 MB (4300326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d13ef4ab459ed56775ec1cf5ac74d3d5f3f899612bbc2dd628beaf590fb36`  
		Size: 200.6 MB (200563055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d0b8121c5cc316d557aeb423992506aa884f60e67337c1e59595355479cb3b`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6494bd74d14cd370421d14267513ef65c51d66d4eb787fa6c862a897043fb108`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47dad8fcc5ae5f475a141387a297bce968218f03e7bcf8987c46b184975120d`  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37854ca880477cc503f17afbec224aec2895a7012a1ce543f9132fac3ad1653`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458215f49b0524389dce9bed7edbef9f9ecbce60988a00c4057200dbb7e379de`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81896b577631381e3f353e8c7cf650af4d7ea728dfe38ce06a53e1bc779c4790`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec2793466c2f7f7bbaa6e618faf0f8d08976e845a2d4156525cde1f4d7a1a91`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.8 KB (4835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.15` - unknown; unknown

```console
$ docker pull percona@sha256:47bf802d03a6547a6c21811f036c010d4b62a099222201b0f67c3b2c67576298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58b6c0dc95e521a3ebc3ad45e341f1e54a76229061428693ece8921fa8ac481`

```dockerfile
```

-	Layers:
	-	`sha256:c1e16bbf53cd9c84ba6e98595b1ea84a36649ab0bca620fa91910f4481dcc841`  
		Last Modified: Fri, 20 Dec 2024 21:29:52 GMT  
		Size: 32.2 KB (32214 bytes)  
		MIME: application/vnd.in-toto+json
