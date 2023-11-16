## `mariadb:latest`

```console
$ docker pull mariadb@sha256:e770695ddbe5192c275c0bedf53826681099a7eda1e927f900d62267048fe922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:e51c275914b2da5e8e8e0ed9eaecf1e4d5142b5e570f231224320001cf5c86cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35870862d64d0e29598fba1d7f75cfefeb3f891cb22b3e2d4459c903e666554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 09:41:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 13 Oct 2023 09:41:34 GMT
ENV GOSU_VERSION=1.14
# Fri, 13 Oct 2023 09:41:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 13 Oct 2023 09:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 09:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 09:41:54 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 09:41:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 13 Oct 2023 09:41:54 GMT
ARG MARIADB_VERSION=1:11.1.2+maria~ubu2204
# Fri, 13 Oct 2023 09:41:54 GMT
ENV MARIADB_VERSION=1:11.1.2+maria~ubu2204
# Fri, 13 Oct 2023 09:41:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
# Fri, 13 Oct 2023 09:41:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 13 Oct 2023 09:42:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 13 Oct 2023 09:42:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Oct 2023 09:42:15 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Fri, 13 Oct 2023 09:42:15 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Fri, 13 Oct 2023 09:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Oct 2023 09:42:16 GMT
EXPOSE 3306
# Fri, 13 Oct 2023 09:42:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb413a01c7e51062c729f32b69c3b714877109c5af99249b5719195f5b47bde`  
		Last Modified: Fri, 13 Oct 2023 09:46:50 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3f76b535d32df1e1b6d9991225a8d848a904dd369845b276143676d1f92d5e`  
		Last Modified: Fri, 13 Oct 2023 09:46:51 GMT  
		Size: 5.6 MB (5592621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7efd05ec01e5adc411f4cb915b9b08dc51606371b92e1f3b1a245dc4c5065cd`  
		Last Modified: Fri, 13 Oct 2023 09:46:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ff83c75dfda686e360e676c7b54eacd2ee02e8c05ce20bf4f2564e0cb80de`  
		Last Modified: Fri, 13 Oct 2023 09:46:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ee0c078c9359ce827ce831452a58adbed812ec39bbaabdd3b05c6dfceff4c9`  
		Last Modified: Fri, 13 Oct 2023 09:47:00 GMT  
		Size: 87.2 MB (87235999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6975e72928bb27788719355cb8a8be77770490f10d36b34ba2c2f0a162e6f3de`  
		Last Modified: Fri, 13 Oct 2023 09:46:48 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d1b426cbdc3b5787fcb4bff535a1361085d373e726eb975c673dd88d840c4`  
		Last Modified: Fri, 13 Oct 2023 09:46:48 GMT  
		Size: 7.6 KB (7569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1060699f5752215be3cbb0f66a72cfbc69ac8970a94035e40e8ae67ad2e42769
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117859615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af66bc898d65cd4cd7d33bb21edeccb4c37d1afe97c602abf28e22da79d6b3ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 02:40:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 16 Nov 2023 02:40:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Nov 2023 02:40:59 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 16 Nov 2023 02:41:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Nov 2023 02:41:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Nov 2023 02:41:32 GMT
ENV LANG=C.UTF-8
# Thu, 16 Nov 2023 02:42:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 16 Nov 2023 02:42:07 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Thu, 16 Nov 2023 02:42:07 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Thu, 16 Nov 2023 02:42:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Thu, 16 Nov 2023 02:42:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 16 Nov 2023 02:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 16 Nov 2023 02:42:26 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Nov 2023 02:42:26 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 16 Nov 2023 02:42:26 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 16 Nov 2023 02:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Nov 2023 02:42:27 GMT
EXPOSE 3306
# Thu, 16 Nov 2023 02:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bfd6232aacadb38909692f1216810e5f58bcc333b7736ed1cb7d166f87202c`  
		Last Modified: Thu, 16 Nov 2023 02:46:24 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda30842f263af44447c78121d344ee924f80a02aaac9c2148e870601433313b`  
		Last Modified: Thu, 16 Nov 2023 02:46:24 GMT  
		Size: 5.4 MB (5406621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b785725f72c47f961a8a68260ac0a1baf821b4d22f7d20a6579a3ef4e6ad087`  
		Last Modified: Thu, 16 Nov 2023 02:46:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc84a6cf47b3bc2b18d39907aca29b5c0b2146e65feaf721a8a43dfd2e7348e`  
		Last Modified: Thu, 16 Nov 2023 02:46:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1c49b2a4731d1033ea03cc4870c8fed929fe80295aa6f9113afc26efa583e5`  
		Last Modified: Thu, 16 Nov 2023 02:47:03 GMT  
		Size: 84.0 MB (84047357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbf01fa668e60ebb31f4fa6e06474aa674433259df513d8f29f2d76865b182a`  
		Last Modified: Thu, 16 Nov 2023 02:46:53 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aecaf7c6c3b661d8598d044d7783b4882bcee194bbdadfa7d9a1b362f1867ec`  
		Last Modified: Thu, 16 Nov 2023 02:46:53 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c180356c6adce55e32012187009100e2e89ad4f316613124be258dacfa06aa9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f82d9a9a38c8ddc592c0953c705c4813e444f5754692a679368bdbcbb28c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 13 Oct 2023 05:51:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 13 Oct 2023 05:51:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 13 Oct 2023 05:52:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:52:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:52:56 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 05:52:57 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 13 Oct 2023 05:52:58 GMT
ARG MARIADB_VERSION=1:11.1.2+maria~ubu2204
# Fri, 13 Oct 2023 05:52:59 GMT
ENV MARIADB_VERSION=1:11.1.2+maria~ubu2204
# Fri, 13 Oct 2023 05:53:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
# Fri, 13 Oct 2023 05:53:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 13 Oct 2023 05:55:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 13 Oct 2023 05:55:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Oct 2023 05:55:16 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Fri, 13 Oct 2023 05:55:17 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Fri, 13 Oct 2023 05:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Oct 2023 05:55:19 GMT
EXPOSE 3306
# Fri, 13 Oct 2023 05:55:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d05729d5870810fd32a20e53e5037ba79b46c20d6d9c38a2e8f68d254cd92f`  
		Last Modified: Fri, 13 Oct 2023 06:13:14 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bac9baac0aaa4bceb71d69ae160ff94fa53f97355bc41df349dfb19c47d677`  
		Last Modified: Fri, 13 Oct 2023 06:13:15 GMT  
		Size: 6.0 MB (6018289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5e7d9fb45ffcf8e04c3e2cdb4f8ace9398f584596be8d3e0d1966fedd5d098`  
		Last Modified: Fri, 13 Oct 2023 06:13:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf581ebaeda1d9b107b00e16408de1c804c8bbcf3267d0a7c5d75cc99d80a109`  
		Last Modified: Fri, 13 Oct 2023 06:13:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544ba3546e326904c8176059279a0aed099483cb47c91a9b25392f90d15f2c0`  
		Last Modified: Fri, 13 Oct 2023 06:13:27 GMT  
		Size: 89.9 MB (89922293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d42823d9e05383a744d26ecf73175b99f317c0838f5b477137b7d5125741196`  
		Last Modified: Fri, 13 Oct 2023 06:13:12 GMT  
		Size: 3.6 KB (3566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377ea8ae4d1493c631d788a65225cb436e9232a5edab6b88fe658c407d161f77`  
		Last Modified: Fri, 13 Oct 2023 06:13:12 GMT  
		Size: 7.6 KB (7569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:4457f62edeaaaedf10e4142220b74a736eb3f49da29adff681d935fde7f4a3dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121882847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2253a03fc0decb2beddf714f194e6854a19475e068e933bc7629f85dce32529b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:29:34 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:29:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:29:36 GMT
ADD file:d165475f8f027ab758a463da57c8c29f5d302f0a87a475ac68fdfae30005c7ac in / 
# Thu, 05 Oct 2023 07:29:36 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 02:32:57 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 16 Nov 2023 02:32:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Nov 2023 02:32:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 16 Nov 2023 02:33:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Nov 2023 02:33:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Nov 2023 02:33:21 GMT
ENV LANG=C.UTF-8
# Thu, 16 Nov 2023 02:33:57 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 16 Nov 2023 02:33:58 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Thu, 16 Nov 2023 02:33:58 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Thu, 16 Nov 2023 02:33:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Thu, 16 Nov 2023 02:33:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 16 Nov 2023 02:34:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 16 Nov 2023 02:34:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Nov 2023 02:34:24 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 16 Nov 2023 02:34:24 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 16 Nov 2023 02:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Nov 2023 02:34:25 GMT
EXPOSE 3306
# Thu, 16 Nov 2023 02:34:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:818e4e246beb9ab026d2b95bf051fe9610b92dbc0a35b45d09b0cf237b6f3c2e`  
		Last Modified: Fri, 13 Oct 2023 10:16:45 GMT  
		Size: 28.7 MB (28650497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaec34821d8eaa6a095ef6e70345e945d226da7e7f888f35a222e5c83c745d2`  
		Last Modified: Thu, 16 Nov 2023 02:39:29 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97ac54483af83269af13d5a0f90572ec8faf79b5c8c2281bbc26ffbef34692b`  
		Last Modified: Thu, 16 Nov 2023 02:39:30 GMT  
		Size: 5.5 MB (5470787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1d1c7d63ba8ddb773cd6269c340ac31b6c2c9b57908a6e91e1f74015c0f92f`  
		Last Modified: Thu, 16 Nov 2023 02:39:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9d32fef99f6095311d54923a2d223bbdd7c305d08a85a4cd2c6eab70f82e15`  
		Last Modified: Thu, 16 Nov 2023 02:39:50 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321f38b6661eb56fa3d040d0bb6682db3c637ec7b8cdcca0ea65a4b9d41454a`  
		Last Modified: Thu, 16 Nov 2023 02:40:03 GMT  
		Size: 87.7 MB (87747856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c91a1c585c5477cbe5c91b7015a1af5bd24d05607fe6699cd5c5ff5bd88e480`  
		Last Modified: Thu, 16 Nov 2023 02:39:50 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0afa2bcb85e79674216b1e22a74e651d74e5c3485a75c5f585d921a49184fc7`  
		Last Modified: Thu, 16 Nov 2023 02:39:50 GMT  
		Size: 7.9 KB (7862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
