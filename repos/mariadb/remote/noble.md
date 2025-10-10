## `mariadb:noble`

```console
$ docker pull mariadb@sha256:5b6a1eac15b85b981a61afb89aea2a22bf76b5f58809d05f0bcc13ab6ec44cb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:noble` - linux; amd64

```console
$ docker pull mariadb@sha256:659a15e38f4ccb2bfa2c7cf824a8a5955fdc5f63cfd01537bc25c9e0ff716605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105535341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbea441e6fcfa4a0396adb35cb63b66ec14738598d117fe2697f32c9cd64a05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7854007237e1b6554e3028be54590e2278e71cf26360abbb4e7b3974b33098e9`  
		Last Modified: Thu, 09 Oct 2025 21:20:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed1b5271813cb22ec4ee7e525ec85602784bb86590b20486e9add63c5a8915c`  
		Last Modified: Thu, 09 Oct 2025 21:20:12 GMT  
		Size: 5.3 MB (5349976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402f4c7dd065b260df399efb60f200e8e6d8f7eb762c69f0aaea7d1a562df531`  
		Last Modified: Thu, 09 Oct 2025 21:20:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2295facceabcdb68f1a001b85bdb9945414b2e740c24f2d6e676a39eb3d87657`  
		Last Modified: Thu, 09 Oct 2025 21:20:12 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eece26ecda4b48efd841525e7a6425debccfb4d8a9e9bb8512ae05018e3c51e6`  
		Last Modified: Thu, 09 Oct 2025 21:20:16 GMT  
		Size: 70.4 MB (70447997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e197f6cb00e857b6cd195af5b31c012fcd826dd5b78920ee43de1a5854c42`  
		Last Modified: Thu, 09 Oct 2025 21:20:12 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6499e85d8558fae3b1ee543e0f61a063671f5a28409c64837f83bbfb0a30c395`  
		Last Modified: Thu, 09 Oct 2025 21:20:11 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:cfdb6df1b156a4928cae0a26143d321ecbff954827a791cb17a7e998e48265a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98cf3ed9d0c1e8a42642ea0b47cacaee38eb065b2a4d0f82ab21a879c768d9de`

```dockerfile
```

-	Layers:
	-	`sha256:bc1aec138d2f6e223759726695023588ba7bce9fd558ac4415c381108cb51853`  
		Last Modified: Fri, 10 Oct 2025 00:36:48 GMT  
		Size: 4.3 MB (4263647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89548bde29bd98445ef39a40b72b8af631e95dcf985909a43cf984036f27d83`  
		Last Modified: Fri, 10 Oct 2025 00:36:49 GMT  
		Size: 31.2 KB (31212 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e9eeec1115df5b11971b719c81805809eea4e809f133796755eba32ade598dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103469744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45e44c1add4457970b964f4d458286e7939050438befcb287ecbe1a850667f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb151588606a8719f9533df3ad1bde5405f0f52ddbc9ace2d075b036f878d00`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e1c4d476db1e4c03917660c85dae36d98e4df8882370b499a50d10188e122a`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 5.1 MB (5131133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d162c7d69fd3c77ab9a3e44dcccc3653be975ac1d4366843d845f3ed2f72a004`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd471cf4bf6df63640714627c5c577b3a02e884de155c0b7193c5662e22ac0`  
		Last Modified: Thu, 09 Oct 2025 21:21:03 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bc6e6a0cd7d4dbb12b711ab34f413645a8998d927e113435274ff9b6bc38ac`  
		Last Modified: Thu, 09 Oct 2025 21:21:09 GMT  
		Size: 69.5 MB (69462676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb64f0adadd1a57f887eb165fccb673975fc72ee586499bd523dde8ad21676`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1a0037b417e7ff249267c53fefd498f61efa8334a7fbf6963b5dd4cc1c01fb`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:f55d779e65921dc9124aeb682002c330db470f583a8756d79ef4372d8b21aa25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b459565b215a1ff28a3ee1769c8fbf05e8cff439c08208b9334645e6023008d`

```dockerfile
```

-	Layers:
	-	`sha256:a48b2f72e52ad0af9584098e41bfcc9ed9d346c29f204b3f4e5e7e80078d8885`  
		Last Modified: Fri, 10 Oct 2025 00:37:09 GMT  
		Size: 4.3 MB (4270922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a314752c7666f399ef234f02726a5caac33efc0b397c4ff88561567be770212f`  
		Last Modified: Fri, 10 Oct 2025 00:37:11 GMT  
		Size: 31.4 KB (31423 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7ea64de52376398bd52e9ce9382b1e9d0e3e835222269ddd3968c8d80c1a1a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115672749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80283fa97fa9a4611d9c783865490ced182e1ca4d4a3c2cc68e193762969a860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d50699c0022fa15ccddfd6888681f19b197f7f91d608cfd687728c01084df`  
		Last Modified: Thu, 09 Oct 2025 21:46:29 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602f6c80f8d9161b95abae64d70adec721ffc24e81c853d867991cf7c45d794a`  
		Last Modified: Thu, 09 Oct 2025 21:46:30 GMT  
		Size: 5.9 MB (5914424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527214ef98f4e0a5a63be5b3d820b718798ecdb7280f43639282746f46c255de`  
		Last Modified: Thu, 09 Oct 2025 21:46:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc6da8dc5716d594099dfdc4d1a287ff1edf9f8dc8939bbfb43b1dc88b5289d`  
		Last Modified: Thu, 09 Oct 2025 21:48:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6218832115ea09908e34b8bad937c5eacb4644973b2786a83000d5a0fdda03`  
		Last Modified: Thu, 09 Oct 2025 21:48:24 GMT  
		Size: 75.4 MB (75440568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf209795cd0c3954b6d904d07a12301966b5dcebb25c632049efac20cbdc4f38`  
		Last Modified: Thu, 09 Oct 2025 21:48:18 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b07273a3f427539c8c94034b35cc8e188bce66fa55ddbe4a015eb2a4fa6a59f`  
		Last Modified: Thu, 09 Oct 2025 21:48:18 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:a75c3d3ebb452e0adb7a42e1e77f41bf01a78e3028942a904266efbe1ef84ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081772c43dee63f1a80ef34a788c647064f52b7df7815667e1f85ccb905474e7`

```dockerfile
```

-	Layers:
	-	`sha256:cedd9776fda023bd94bc238b0ced32fc3ca7d0834e682b875aa89f9d17138c77`  
		Last Modified: Fri, 10 Oct 2025 00:37:16 GMT  
		Size: 4.3 MB (4271568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98a0743d6bcf815e8906a3eda61f58bf237caf9cbaa3e00f126f39336041927`  
		Last Modified: Fri, 10 Oct 2025 00:37:18 GMT  
		Size: 31.3 KB (31288 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:a063f1a384d2923f29589b26520af2d066a9b5290daaa1c1810259adf8b2b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110916307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883145c7c417e15fd4a3811ba2abfe350d2350d93e353065863af865ce794414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf236dcd2206679587c3539356a1919e73ae88f6eb34459c5ce6e8f2848392`  
		Last Modified: Thu, 09 Oct 2025 21:44:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a38c3c456c091e450b1c4732752b74aeb640fc961e73b37c45cf68f34fd2a8`  
		Last Modified: Thu, 09 Oct 2025 21:44:15 GMT  
		Size: 5.5 MB (5483487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f78f492c8d08d815d235d3025de11602cd94353e26d6a4a122c5b4c1781ea9`  
		Last Modified: Thu, 09 Oct 2025 21:44:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192bbcfb76b772cec679c3023f433533fce584df94f99bc5f9f8a1afa8a7d915`  
		Last Modified: Thu, 09 Oct 2025 21:44:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0c10b2e84b08e04c6f93dcd44cd3002698fa7ca0e4106490e1faad89bc22a5`  
		Last Modified: Thu, 09 Oct 2025 21:44:19 GMT  
		Size: 75.5 MB (75512441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bdaee91103346ed73b035797d6b166be3e62e14e0fc8a0f49f059b197d4584`  
		Last Modified: Thu, 09 Oct 2025 21:44:14 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc73c2336ac0ef46cf65ee6298ab3709957fc745d60ad893749b0ab2ce7731`  
		Last Modified: Thu, 09 Oct 2025 21:44:14 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:dd86672d35871d8c83b8d90f4d8ca18a0ca9efc2605a7ecd73cbe76100c69b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edadb7161f2db32fa557424eec469fbc11b6ade8fb8b25b4ba9fc61fede321d`

```dockerfile
```

-	Layers:
	-	`sha256:8f4182ab3d90a897c4b63ee71019236ec91a560a23be7ff54865779361c744b2`  
		Last Modified: Fri, 10 Oct 2025 00:37:23 GMT  
		Size: 4.3 MB (4265368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd45fe80352b3a7d9a28d6fa3f1d91edb5e595efea189aecd97b2621b3823d57`  
		Last Modified: Fri, 10 Oct 2025 00:37:24 GMT  
		Size: 31.2 KB (31212 bytes)  
		MIME: application/vnd.in-toto+json
