## `mariadb:lts`

```console
$ docker pull mariadb@sha256:196329ec891258644741b0273232550778d523e56ce69119e70d0429f0dd0050
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

### `mariadb:lts` - linux; amd64

```console
$ docker pull mariadb@sha256:9586c56a4e039ae5978d2aa0b2cd06d2e5a94844db6211baa0fe04ef5b38504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124599578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd47cd36095d4dc564959cb716f12e2bd38e2d65def2b65bef8b23488d330dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV LANG=C.UTF-8
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f48130ffdc66fb60cf0fcba8c31a4cec0b36b873dc5913f4f450d56830622`  
		Last Modified: Mon, 12 Aug 2024 16:56:32 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef8be0e9a2f51b9a8b83610b6a59f6683243dc449a672332ca0c21461840008`  
		Last Modified: Mon, 12 Aug 2024 16:56:32 GMT  
		Size: 7.8 MB (7753800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442cfde7be3679e4c34f8fdac9b1263f8dc3d970e25e91ad5ab8762f7d3528c`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104b8687cab891c8e141bad864ce5f84e0f2ded6d6246629a4f80cfebc36535`  
		Last Modified: Mon, 12 Aug 2024 16:56:32 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e6c2ba968158d2b80f9d814cfe4b4e24506fabdeb50e7302a7ea2fbf80270`  
		Last Modified: Mon, 12 Aug 2024 16:56:34 GMT  
		Size: 87.1 MB (87126562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ea4b4fc2183fbc80407cf346e6bc105744555d79689dbdd2ba9d11ccdc440`  
		Last Modified: Mon, 12 Aug 2024 16:56:33 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9225d071cdc5c59afc61746e6f5c2f22cb99a28713d39ba3c147dd2ac8ea763c`  
		Last Modified: Mon, 12 Aug 2024 16:56:33 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:85f6d3857084404759d1f272bc2172cc232b89f5c0ba9bd0695201f86162d00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4c6b4c021804db42c7e3518e7f94a2b3b475fab316f55e54292f277ed2cc26`

```dockerfile
```

-	Layers:
	-	`sha256:34ddcda3d1d358425efe9f61de174b938b9477152f2a1297264cec5f409b96c8`  
		Last Modified: Mon, 12 Aug 2024 16:56:32 GMT  
		Size: 4.1 MB (4060635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee0ef4c98fb735c780cbd01a6f1a12629f18eb2a7a58c1fc89a456e08c09d2f`  
		Last Modified: Mon, 12 Aug 2024 16:56:32 GMT  
		Size: 31.6 KB (31574 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5dde1f996e769f91b15d37af1f8f98640dc3546dbd9757ec6633f14be73ffa09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122459130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c86abd16627adb28a7aec05df2dc2c11301cc9f670342ecc81f9c2ede2f3b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV LANG=C.UTF-8
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c5d2885b1c0e6cbdb0b443943449563675454ea7e57fc9e69dc253e31dce41`  
		Last Modified: Mon, 12 Aug 2024 16:59:48 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9965947b66161618059dceec1ddbebae41346cfd423e7dd35687007d8dd5c4b`  
		Last Modified: Mon, 12 Aug 2024 16:59:48 GMT  
		Size: 7.3 MB (7349918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bd3e837e83b7d42e1745b4ae48042ca9cd84c269795a76dd9dff09af207bf6`  
		Last Modified: Mon, 12 Aug 2024 16:59:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d36dd2121d2956ad4e7ac4e094204ca5c1acec8040b4beecef5a44b3211ecd`  
		Last Modified: Mon, 12 Aug 2024 17:01:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475f0cf1b9673e45abb3993799f4e8b119069203645aec2a7626348ad9fdae82`  
		Last Modified: Mon, 12 Aug 2024 17:02:02 GMT  
		Size: 86.3 MB (86252109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720cd418c05c8552ef474ff625fcf6c222438e4138f12d8fcef24509bc26f794`  
		Last Modified: Mon, 12 Aug 2024 17:01:59 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d74759a741dcc778cd416e8badb7daba18d647de43ad3aa5a4aeda2b9e2c8e2`  
		Last Modified: Mon, 12 Aug 2024 17:01:59 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:dd1cca1c5e1bfa3423f2242b779878e86bac50eaa7133cacda762f409057c6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4099884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56a0284f5de8fcaf9118f84a0052d83834bc01f3bafe5e23044ab083f08804`

```dockerfile
```

-	Layers:
	-	`sha256:54f7dbb214a6c46414d636cf5a3bc9a213c051872b072e142365365be16c142a`  
		Last Modified: Mon, 12 Aug 2024 17:01:59 GMT  
		Size: 4.1 MB (4067938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9814419e377ad0582a2549acab068563be2ea5257058739008c029b925b6daae`  
		Last Modified: Mon, 12 Aug 2024 17:01:59 GMT  
		Size: 31.9 KB (31946 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:89e47d5278dd0c99f0c7a14e9387bab935df54bb15d2fd7f7bb2d8bb495dcf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135607769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b57efb502f4884c3a646d8906706e4827fe64156da35ba623521466d94e3070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV LANG=C.UTF-8
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c960adffb44ff684629bad18162098aa80bdc47de68af0abc8d3677716983`  
		Last Modified: Mon, 12 Aug 2024 17:00:07 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737d1a417262cdf487ebab733deecd58760dd51a227af9e336a532d2586fc936`  
		Last Modified: Mon, 12 Aug 2024 17:00:08 GMT  
		Size: 8.6 MB (8607131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06debcba18a1d73f7516c3487e0da52fbdf048b52610ae188fb853456ed478f7`  
		Last Modified: Mon, 12 Aug 2024 17:00:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541551314d37d12a66c829ca30732c4013961bf09b8c404b257f82f4605e00bd`  
		Last Modified: Mon, 12 Aug 2024 17:04:09 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f9c2481076a5b60ad0b9073b1b396fe68f7d84bfa1f5ab66ddf4942d6e7bb`  
		Last Modified: Mon, 12 Aug 2024 17:04:12 GMT  
		Size: 92.5 MB (92480543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47059d53be312b869b589de11a45b078cc4cd9a1a7c651f7803ef425e583d2b5`  
		Last Modified: Mon, 12 Aug 2024 17:04:09 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01177677dc698c171cf8f30dd1ce605cc40597f154aac04fa23d69e9b4c659f`  
		Last Modified: Mon, 12 Aug 2024 17:04:09 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:3f9d86e9da7e4518d5eb8537fab951827cf0a7c44b97656b69d1536b9a6b1ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4100051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3300013c8cdcaa590c2b45b256976dcc0aab8d24bb4961c07e551be5fed13fe`

```dockerfile
```

-	Layers:
	-	`sha256:2680ae0337c5ae3f03de8505975bc1c84ec81323d889cf6807a11b0cc15964aa`  
		Last Modified: Mon, 12 Aug 2024 17:04:09 GMT  
		Size: 4.1 MB (4068395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f462a9d9ed977c3236420237d337945c452f9184909d304b31e959c0e7e4003e`  
		Last Modified: Mon, 12 Aug 2024 17:04:09 GMT  
		Size: 31.7 KB (31656 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:f78583006cc929ecdc5df24921f4322e18e73e47098990c6d77c516525307c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131062285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d1a8b13a3646730133a01f856b6f5975a65a6aca1be8cc5bde714e474023f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 23:52:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 23:52:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENV LANG=C.UTF-8
# Thu, 08 Aug 2024 23:52:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 08 Aug 2024 23:52:24 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Thu, 08 Aug 2024 23:52:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 08 Aug 2024 23:52:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 23:52:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 23:52:24 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 08 Aug 2024 23:52:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03beda01fb72956e748d017421f02f854a51a9970b9412ea4b140330631c973`  
		Last Modified: Mon, 12 Aug 2024 17:01:49 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d4d4bcc2da149cbbe4cd9198db4b92be25a56be1a6c42718ac064638326edd`  
		Last Modified: Mon, 12 Aug 2024 17:01:49 GMT  
		Size: 7.7 MB (7657300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab932857bb012d96cbcf7bcaf6268d4c5df0e4a244e43e00239f97793b875`  
		Last Modified: Mon, 12 Aug 2024 17:01:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b919f4991c7a7a37b91e1550db34bc4597c693ed8e8ad434fd71244bd53049`  
		Last Modified: Mon, 12 Aug 2024 17:06:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afecd12b5f73dbb09b409499b9c559e8cd16524786857010833dd2a2485cefb5`  
		Last Modified: Mon, 12 Aug 2024 17:06:20 GMT  
		Size: 93.3 MB (93345229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9cf3fdbf6db5c39cfa67859d41e1c77f9bdf1a281cd35d5228d06e54842ba`  
		Last Modified: Mon, 12 Aug 2024 17:06:18 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83137eb2d1a05aed7e28296cfdad8303c4fc986afb1864922b56ee63c768009`  
		Last Modified: Mon, 12 Aug 2024 17:06:18 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:322a6f43a9c4d534f1a8fe57c081041bd2564c1209629dfb66450d2cbc65fecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053e43ab2554f102ee4eaaa6ea3f022767809a69ee5faadb4d4c805523e99748`

```dockerfile
```

-	Layers:
	-	`sha256:2dc130ba1a141507951bf75881d60f5e22c1917581e48bace57ba3b5079e50c2`  
		Last Modified: Mon, 12 Aug 2024 17:06:18 GMT  
		Size: 4.1 MB (4062363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027b684fb4a1ecd5541c57a687d620bbc62ea94f806caa67738170d9d45249dc`  
		Last Modified: Mon, 12 Aug 2024 17:06:18 GMT  
		Size: 31.6 KB (31573 bytes)  
		MIME: application/vnd.in-toto+json
