## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:40843b253d7b21fa83b10b8f0b4cf538e1c90bf4639fb3a2818f82ea0568172b
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

### `mariadb:lts-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:56cbf210fe2baa9cb89f6ebe95507148c419e3005b08ce9c0b1a480b426fb80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122390246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b7ba1d0a4610f56ae808609034e68dfefef4d1f9b47878da9552ba9d33486d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3637fa016ac979357d44dcd2e564505144c86953cd6cb628e96fa0943161b976`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6d6a06705b91a350a9db09f7fa5c0362b7d94f0962c50a54760a03067dc67c`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 5.6 MB (5646082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70743825812573e3ab82066006afa941138fc387f374dd6a36e0ca6bcc6861f8`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59ddf39624d26c94cf28255db1ffbdc0a8f9d408f6ee230eb4da8ebb7890b92`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52060eb12a31e912b52dab21a6628553bd88307c97d73c9abe44f4955720a7d9`  
		Last Modified: Mon, 08 Jan 2024 22:57:40 GMT  
		Size: 87.2 MB (87183039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289355ab1d30d26bada8a08e84d8925a8513149bb3448b200dd47c221a499e86`  
		Last Modified: Mon, 08 Jan 2024 22:57:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb478883dfdfff4543498da35c695f800a7dec92b43ca810a55341d289214459`  
		Last Modified: Mon, 08 Jan 2024 22:57:38 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:2e3713dd6477592b94d708d91caeddfa8b34c8a734834ce5ec1165b74dc5a138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c7c499b1a694b13e95afa7431e5e4028bfe6ec7d4664453a5a2de14acd0105`

```dockerfile
```

-	Layers:
	-	`sha256:808ddb6e7674f1d3b48b3c2867173baa49a8ccc88d87992c09e286c82023e3ad`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 4.0 MB (3977505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128e2caddd67c80b138b43de07ddb2999b3a32091029107aad125c4eaf59e916`  
		Last Modified: Mon, 08 Jan 2024 22:57:37 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9e39af854e863fb1daa0381e763b3257796ca166d6ca697cb79d05dea847bdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116768801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b04d367d07d4833e7a7e747f39ee1b84db1bc535827a7b30103c9e7db6315a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e465b63f30111127b4c2f1a4297c9733c1c225e40ea2d3ae600e63f33832f4`  
		Last Modified: Tue, 09 Jan 2024 00:06:30 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b23153065d5051a31b841a91174e0590015049d53824f29f3316e88163dde4`  
		Last Modified: Tue, 09 Jan 2024 00:06:31 GMT  
		Size: 5.5 MB (5461267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31229f1eeda20a67714a58c055710e7c4e138cb8a3bc9be09eaeae3819fb4f`  
		Last Modified: Tue, 09 Jan 2024 00:06:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa7534b28aaf79d804735d9fe49064ff82b3b89d2f81e7f694d49a1aad7ffe4`  
		Last Modified: Tue, 09 Jan 2024 00:10:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b0d07db0c73120f53df9d7a8ce6e8b5d71daa424fd486849e1a6bc051c322`  
		Last Modified: Tue, 09 Jan 2024 00:10:13 GMT  
		Size: 83.9 MB (83935646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b4a45eceacedc16e84ca1ec8bdc1c8d9f1101c1230a1f9f980cc6a6168686`  
		Last Modified: Tue, 09 Jan 2024 00:10:10 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cb46e04d3bb0b97b7fd14be9764ccb70608a7b4bae4475e2e0c56615c80ae2`  
		Last Modified: Tue, 09 Jan 2024 00:10:10 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7742668559d4a80c1c354925a5b91dce1cc9807195ff41e22e1e220189f97b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60f2dec38a04f2a45ab8816675eae210a8e4dd1582b387490fe396118b6ccf4`

```dockerfile
```

-	Layers:
	-	`sha256:fe4ab866875e170eb6b8a2c40d2d47091f6ef17dd0c7f8bc9d9edf7e094cf95f`  
		Last Modified: Tue, 09 Jan 2024 00:10:10 GMT  
		Size: 4.0 MB (3983253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844ec206422b0b7f060e30b4e4325a9578645ea301cb514557911130c1bf0f50`  
		Last Modified: Tue, 09 Jan 2024 00:10:09 GMT  
		Size: 31.0 KB (30992 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e98ec93095d8783b7f8aa8dcafc2349f5bb9cc966be8295f44d16587465377e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130489876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4171500fd13f5bd33b5a7e7d8d1c5b17410a92364939eb987b5d87164326634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2aad393e0d6df69496ca22adeeacd332fb9130e324fc58fb3bfa0565b8ddf`  
		Last Modified: Mon, 08 Jan 2024 23:16:55 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0482e23d8c1aa6dc3b7b551a4492877847d406c90de4819fd6841f4689156ea4`  
		Last Modified: Mon, 08 Jan 2024 23:16:56 GMT  
		Size: 6.1 MB (6078290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48d3cd3b10c5db8463f0f848544080cea38d4d23858d1b723e39719a2972ce0`  
		Last Modified: Mon, 08 Jan 2024 23:16:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65f2517c72ee3501a9953fb18c26d7750de32f071ca9cb957db09fe2c278894`  
		Last Modified: Tue, 09 Jan 2024 00:11:03 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1304d406d907c52c36ecc78ba3fe04afeaca215abac8dd1bbd29acc1aad7bc6`  
		Last Modified: Tue, 09 Jan 2024 00:11:06 GMT  
		Size: 89.9 MB (89876327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7facaae12342ded0533f40eefbeab16008add9313732dd1db6d7b8c307d66ef9`  
		Last Modified: Tue, 09 Jan 2024 00:11:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab329c87367ea5c9282b749830c528291e5457626e2fcf55c2ae8e6e9fe2668e`  
		Last Modified: Tue, 09 Jan 2024 00:11:03 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:0d057196bcffc3d011424882ad3a63ac8a7afd54bee853ea37451b9b2efda522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d28fdbb571981bc2dbb976eacad201b8a5b2125e0f87db93ea807c15c46167f`

```dockerfile
```

-	Layers:
	-	`sha256:b0eeeea9d054e132d35aa92951980e20428f6b1df4901e89266ca3754fab697b`  
		Last Modified: Tue, 09 Jan 2024 00:11:03 GMT  
		Size: 4.0 MB (3985176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522c5c10db0cc80ac507839943e600d4cfb9c5ffe3f2639f1a808f17259b57c7`  
		Last Modified: Tue, 09 Jan 2024 00:11:03 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:845526dda36ddd936f216588553ea9674b8459878072dc8e7ffe7820862a8245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121199858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38ff6169887fee2a67d2a6aea3ee870c0465df76cf231c198ad59d792e06b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0585c95fb8c14557239710cff2bcbe2bb41092592fe516d12f59655090a375`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ccf50449c795b6798ec8592b12cc3c4e7cf094455d8a086aefa37d0700532d`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 5.5 MB (5530655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07704ca35080050de0a45a34808769825631ba57e4ec6e9e7820c42845f9c5a`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0147630a578715ee901dac17cb2c53fc118c680c427e3fe738265b85e7fe979`  
		Last Modified: Tue, 09 Jan 2024 00:11:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9320a1cd6642532fd8364b632b074292d2deb5219da3beab96def623f661e2f2`  
		Last Modified: Tue, 09 Jan 2024 00:11:11 GMT  
		Size: 87.6 MB (87628366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973119448830b53cff38d00e91c94150d091a1c8cc20a9883a0ec16baa3d4801`  
		Last Modified: Tue, 09 Jan 2024 00:11:07 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353ea0d526dd3a08ebe03354bbeebc4d1b8225837ffab7680f2efbb519abadb9`  
		Last Modified: Tue, 09 Jan 2024 00:11:07 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:84160cde60c9c489126b1dfb609a167c1182b4e6be012b537b49e42a0ffcde37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b356893962c976f15e6cf4a24b4eee602b11b67d20e931241252930de2d50803`

```dockerfile
```

-	Layers:
	-	`sha256:84c3cda58ea280f5c9377967098e277a49878e6029777c5fdf5f19dc6919de3a`  
		Last Modified: Tue, 09 Jan 2024 00:11:07 GMT  
		Size: 4.0 MB (3955501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2b8025fbb74274aa7d623dbcc7aa1a662e13e9496a0dbc5f342d023e947c5d`  
		Last Modified: Tue, 09 Jan 2024 00:11:07 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
