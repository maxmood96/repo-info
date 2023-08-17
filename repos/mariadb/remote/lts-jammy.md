## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:82e25b84b1d413dc1d57a8cc4511deb4e69b62690080ed11a4f7013815f19bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:lts-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:d38528a682f806b8a3d0ecc5347ab9eca6ae2228002f197fa9ed2fd95598634a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123137969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9846a42c7bfe5349bf60808f0ac4c57101a6ae87ba52f7bf0c462fb461203974`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 16:03:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 16 Aug 2023 16:03:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 16 Aug 2023 16:03:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 16 Aug 2023 16:03:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Aug 2023 16:03:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Aug 2023 16:03:37 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 16:04:31 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 16 Aug 2023 16:04:31 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 16:04:31 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 16:04:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Wed, 16 Aug 2023 16:04:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 16 Aug 2023 16:04:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Wed, 16 Aug 2023 16:04:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 16 Aug 2023 16:04:49 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Wed, 16 Aug 2023 16:04:49 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Wed, 16 Aug 2023 16:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 16:04:49 GMT
EXPOSE 3306
# Wed, 16 Aug 2023 16:04:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98349557ce71c917468ad0d23ca6dbec00d6c82f427bdbbf370dcc706ad2f5e9`  
		Last Modified: Wed, 16 Aug 2023 16:06:14 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310e8807220b3c547f4333da24d331e6cd9b2ea7fddf668d18081858d6bb5ef`  
		Last Modified: Wed, 16 Aug 2023 16:06:14 GMT  
		Size: 5.6 MB (5592726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d75d8e504d1714694629bcfc2e1c63f2f9e1d3c3a9254d9f158af95ed6f73fe`  
		Last Modified: Wed, 16 Aug 2023 16:06:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417f49d970035aa3fcecc81f84e7a207d5105bd420beb55eaf6ea028e6013e6f`  
		Last Modified: Wed, 16 Aug 2023 16:07:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e9da41589276742c6217eaa21991e6fe4d608dc125ca85f9123d146cb1fc90`  
		Last Modified: Wed, 16 Aug 2023 16:07:23 GMT  
		Size: 87.1 MB (87093922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0396f9d9ce8397bc8e9c8f9ca0e2835e346b93995edfa69299fdaf5bf665bf`  
		Last Modified: Wed, 16 Aug 2023 16:07:11 GMT  
		Size: 3.6 KB (3564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2d50d7ed80bd86b352e42b5d17a8ed980e1224b9132c39ea4f7e3cc56d8960`  
		Last Modified: Wed, 16 Aug 2023 16:07:11 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:da99039994f1b5de2971c4579314e13e21e960e48539cc4d7495e480974d7c11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117666213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac2017cb581b313a1ba3772aeb5311167d2dbd9609f9cb1abe5cf555f9dd09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:41:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 16 Aug 2023 14:41:14 GMT
ENV GOSU_VERSION=1.14
# Wed, 16 Aug 2023 14:41:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 16 Aug 2023 14:41:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Aug 2023 14:41:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Aug 2023 14:41:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 14:42:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 16 Aug 2023 14:42:25 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 14:42:25 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 14:42:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Wed, 16 Aug 2023 14:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 16 Aug 2023 14:42:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Wed, 16 Aug 2023 14:42:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 16 Aug 2023 14:42:44 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Wed, 16 Aug 2023 14:42:44 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Wed, 16 Aug 2023 14:42:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 14:42:44 GMT
EXPOSE 3306
# Wed, 16 Aug 2023 14:42:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc549d832fc3a0da813bf41e9b2a5e7429c23a3eb9ec71c05130170c731bf03a`  
		Last Modified: Wed, 16 Aug 2023 14:44:02 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e7c4d471f498c86b82789133fe6932f833b84f09b6f732585ce47927b9037`  
		Last Modified: Wed, 16 Aug 2023 14:44:02 GMT  
		Size: 5.4 MB (5406689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc486e955e858b609a50e308c893d34801b412cbe18e215aed0428a820e4d3`  
		Last Modified: Wed, 16 Aug 2023 14:44:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048cf39155759bcdcd258f1b408e9aede277f19c9672a745037522fe84b5a580`  
		Last Modified: Wed, 16 Aug 2023 14:44:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef147633097572978fc3a88baa9d4f13fa9d777b2864753abf4737f14c9550`  
		Last Modified: Wed, 16 Aug 2023 14:45:04 GMT  
		Size: 83.9 MB (83854252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20b0190af67a3d415be2a948ddcd2c0fd1ab0e910dcbe2ba72b55a045cb1738`  
		Last Modified: Wed, 16 Aug 2023 14:44:53 GMT  
		Size: 3.6 KB (3564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157392f528e0e89cc0d125a05520514bd220625ff8923d2bd9c06a9a90ea799f`  
		Last Modified: Wed, 16 Aug 2023 14:44:54 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:42c362d72933560837399591b5dea2ecc4aaee70ca2a0e36378ea248544fcebc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131547573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56cd33e7f6b9442195aabd40d76b6ca4d29b8dd4847dad3649a3f3bb6aaa249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 08:09:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 17 Aug 2023 08:09:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 17 Aug 2023 08:09:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 17 Aug 2023 08:10:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Aug 2023 08:10:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Aug 2023 08:10:01 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 08:11:55 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 17 Aug 2023 08:11:55 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Thu, 17 Aug 2023 08:11:55 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Thu, 17 Aug 2023 08:11:56 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Thu, 17 Aug 2023 08:11:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 17 Aug 2023 08:12:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 17 Aug 2023 08:12:33 GMT
VOLUME [/var/lib/mysql]
# Thu, 17 Aug 2023 08:12:33 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Thu, 17 Aug 2023 08:12:34 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Thu, 17 Aug 2023 08:12:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 08:12:34 GMT
EXPOSE 3306
# Thu, 17 Aug 2023 08:12:35 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2848525b96e14ec0caec7c497809d28b4d5be3035ea274337f81a62011122381`  
		Last Modified: Thu, 17 Aug 2023 08:15:00 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c242686148915edc570f0fa45f6b0709a88d3769452a4c5a95b579b2384985`  
		Last Modified: Thu, 17 Aug 2023 08:15:02 GMT  
		Size: 6.0 MB (6017996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0acbb82d273fd443fb63852ca4a04d0eb6c4d4717c673529771a1121474bb8d`  
		Last Modified: Thu, 17 Aug 2023 08:14:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4006bcc5c4bc7e2a97d80743bb00ed397c4589fc316ec1fbf8aef22c543e16e2`  
		Last Modified: Thu, 17 Aug 2023 08:16:39 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7510cd7a25930b9ae6da1e5c1d3e34fbd11ddb55f5a0f4bf70ac38629b952f60`  
		Last Modified: Thu, 17 Aug 2023 08:17:02 GMT  
		Size: 89.8 MB (89803523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d711e06a4089ec922b64ad2f3d690684c36e7efcd6c1dc2bfe8ef75489afab2`  
		Last Modified: Thu, 17 Aug 2023 08:16:39 GMT  
		Size: 3.6 KB (3562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e33961dc8acb4efbbfd694d45bf5023fc8b395ccd677955dc4339c0b74d11b`  
		Last Modified: Thu, 17 Aug 2023 08:16:39 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:6c2b2237a09e44947bd2881d6a3d98ecfba74e498b217f68c0deb1edaa6bf3d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121642596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e91ef7969b72d0f8d3b2ee66e18e500e4e3eddb7436466fd1f812c8dcc359c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 09:36:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 16 Aug 2023 09:36:16 GMT
ENV GOSU_VERSION=1.14
# Wed, 16 Aug 2023 09:36:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 16 Aug 2023 09:36:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Aug 2023 09:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Aug 2023 09:36:36 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 09:37:55 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 16 Aug 2023 09:37:55 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 09:37:55 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Wed, 16 Aug 2023 09:37:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Wed, 16 Aug 2023 09:37:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 16 Aug 2023 09:38:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Wed, 16 Aug 2023 09:38:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 16 Aug 2023 09:38:18 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Wed, 16 Aug 2023 09:38:18 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Wed, 16 Aug 2023 09:38:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 09:38:18 GMT
EXPOSE 3306
# Wed, 16 Aug 2023 09:38:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:de1d106061fc0332ca262e39ed7d2aa6384ae341a084b39449e21c742802df9c`  
		Last Modified: Wed, 16 Aug 2023 04:39:02 GMT  
		Size: 28.6 MB (28644373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cfb5930fe1eb6681c4536fcde511cd2ff74a08a9d54709fbb5d5334e34e6ed`  
		Last Modified: Wed, 16 Aug 2023 09:40:00 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793b8aa0e7f4622bb4e33b94a209b753614409638f0ac6921b09a4d708868752`  
		Last Modified: Wed, 16 Aug 2023 09:40:01 GMT  
		Size: 5.5 MB (5470855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78926922caa9c1d6e5a2ff935b67e10b92c834135521d516e689198ace96830`  
		Last Modified: Wed, 16 Aug 2023 09:39:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1d94f4b12bef8f241bc537decbe3baa86981034cf48d3848a3f805c04ceb12`  
		Last Modified: Wed, 16 Aug 2023 09:40:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e48aa21b15208e2b213a05a3c66a414d90c7f3009b3f4a88763d425604258c`  
		Last Modified: Wed, 16 Aug 2023 09:41:00 GMT  
		Size: 87.5 MB (87513999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2d9fac57ea1092bdcfcf5f9866c26ed2323a433acce4516c0a9187f4635e29`  
		Last Modified: Wed, 16 Aug 2023 09:40:47 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda4ae9f305f690846a65eda43a9adc4e97e1c5d7f291dc2118fbc1fe060358b`  
		Last Modified: Wed, 16 Aug 2023 09:40:47 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
