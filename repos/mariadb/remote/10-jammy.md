## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:a0e299dce770c298fc7cfa4039205c066afc534ee6b72df8fa03cd3b151af938
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

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:905dd2ee9f25eca4f8e916dfa9e008c817972bf3f9dde64bd0430952adeb8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122463761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9200bd86da810533901767e7211ee0accd4d5a762792e6f4d7bff4c5210eb910`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089a232b2831d8e7431fb722d6e03b77b448e93db7b085c592bd41f96fbff21`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a7853251a98ea10f21d83a3ca32851e9cd1dc66844f16712f06eb1dfc066c4`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 5.6 MB (5647564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c50173b460214bea4f3c189e58df2ef0507e7cc8741b05d923bbb3241d49a`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cf01d97b1c67b821dd3f8376b6ee617cf20ce5c59786f5f72b8769e9fd5bd2`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8712b8a312886962d548b6c36e24ffc58179421c58e948b41336064dc5757d9c`  
		Last Modified: Thu, 02 May 2024 00:52:46 GMT  
		Size: 87.3 MB (87268222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2713dbe305278e228b89692f63452929c76728e2f687035cb055dfd8bc85018`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ffb22994e641d2318675c9441c73b2028242ab620867cd2d58d2f40193dc73`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3f7abbdb77609f2febe207bccfe6b434b62288dc8f81b0f7ad6084c90918e9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4609181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980d7c191665abe99fa328e5bf9b2b22447302ae2ceef778cac7c93ae2b966fa`

```dockerfile
```

-	Layers:
	-	`sha256:267390f8d1a6f30632e04c9ebb2f76f08a28d403cb8009b82442b892c18bf323`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 4.6 MB (4577747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44eed940f67aeb472fe90d814746e7bd1e92a1012481b13e6453a06ca97917d`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 31.4 KB (31434 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6efd2212600f7ce84959b22ecd3ef7ca0cf96ed9528d5878311fde8bf7ef9aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116868775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bacaca4bc3806965484928ffa532f0f9e932b29f95e08adc9b1add41cd1f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ef8879b7897601a39e1de82a5f2c44f77b7ce9c9d504f735a3fcc247197bbbfc`  
		Last Modified: Wed, 17 Apr 2024 18:55:35 GMT  
		Size: 27.4 MB (27360350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cbf2cf67ddebca4fcc5ac79d998dfe00417adcf365f7d8cdc561b03306ecd`  
		Last Modified: Mon, 29 Apr 2024 17:19:19 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf1df91ceb62a4d59fb7f4127546f7db47785fbc39430747aa58392c6426633`  
		Last Modified: Mon, 29 Apr 2024 17:19:20 GMT  
		Size: 5.5 MB (5461041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8390621d2f876b8833fd13e0936e6c0ec1476e6256d4f3bab495fd0c604ccb`  
		Last Modified: Mon, 29 Apr 2024 17:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc86ad8171dbc12fa75fe4b1dba3f6d035bee6c437e3ce6843e0f993ec6b933`  
		Last Modified: Tue, 30 Apr 2024 02:04:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d9ce0bedea3eb8873b7279321242e81ceaa546ab39aab6a7cae9119889753`  
		Last Modified: Tue, 30 Apr 2024 02:04:06 GMT  
		Size: 84.0 MB (84033344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a02c9f73be2e6903dca8becd17e54243760210b201b6d2d41f3a365391bde1f`  
		Last Modified: Tue, 30 Apr 2024 02:04:03 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abe11aa4efbfe8f5b1c896ec2c2e6a3d291081657e3abeaa239994e928d4b7f`  
		Last Modified: Tue, 30 Apr 2024 02:04:03 GMT  
		Size: 8.2 KB (8247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:8aa8bb7e9121b97f58de4cb106ef92bfacbc09c9cb04113db1bdcbc82e0ce3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4615422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d39ff615db409a17e6b4a4008c30cfecaec412de33eaf09eb93564017ca64f9`

```dockerfile
```

-	Layers:
	-	`sha256:883da6515cb781ee9c86932dfe7abcab5336f8745f71c4b69f2b7875f2c5655a`  
		Last Modified: Tue, 30 Apr 2024 02:04:04 GMT  
		Size: 4.6 MB (4584131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd52327035283d9b79095df38ef179d84ca6d90d7537958d0158625ae7db7b4a`  
		Last Modified: Tue, 30 Apr 2024 02:04:03 GMT  
		Size: 31.3 KB (31291 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ed1520ed13e6bc4a463618e7c95d5bd0ace73a9df61c3a94f25cb8844a56a02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130516975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c587804e75bdb8f10ddf759631a35750d867ba2f0dfcb358d9abe9ef32003bb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8735f03877b4ef190c5279652cd5a0a8db5ddb4170fd1fb1710abee9d2f811b1`  
		Last Modified: Wed, 17 Apr 2024 18:55:49 GMT  
		Size: 34.5 MB (34461311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c70ad7d6e03634799f516541da6fba8cd0b3fa69fc8281197bb5507ee5f4704`  
		Last Modified: Thu, 25 Apr 2024 23:10:00 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76147975155474fcc9b3236571c1ff5a666122ca0a7f1ef93002240f0534707`  
		Last Modified: Thu, 25 Apr 2024 23:10:00 GMT  
		Size: 6.1 MB (6079554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cbf8ceae33172414902f56988d2b960fe0e71e546a6304ce00938d5c1d55`  
		Last Modified: Thu, 25 Apr 2024 23:09:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b8cfe585a775f506ee26b033dad9b28ef5a11bbdee17e189304ab9d4b6a7c7`  
		Last Modified: Fri, 26 Apr 2024 01:39:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1721f043c033973730e81ed4c251d19ef981df490dc2d4c544583b16b2b6fcfe`  
		Last Modified: Fri, 26 Apr 2024 01:39:18 GMT  
		Size: 90.0 MB (89962064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace20b2aa033b0d94d79b6218353cb686ffa907466ba0a00a9fe3257d93c113b`  
		Last Modified: Fri, 26 Apr 2024 01:39:15 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422368a9a70742e59748aefca6d7653f1e877fff2d8d46b7bae50587119fce87`  
		Last Modified: Fri, 26 Apr 2024 01:39:15 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:210bd8e6d68fdab4cfc01d95e878949d27569847d0b69be868ac61cb8916f82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ee69f5240f8fd300a38ba30a6198c411efb9636974841164a71a5b8e7194f`

```dockerfile
```

-	Layers:
	-	`sha256:1f3af8317c7100d7b3d02822f52783f986576b7185e7ac9d56f34afc822852d1`  
		Last Modified: Fri, 26 Apr 2024 01:39:15 GMT  
		Size: 4.6 MB (4585418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f10d198c6a8cbb7b6553fd14f1b9225c80b9c2f0cbf4ab60807e1762610a842`  
		Last Modified: Fri, 26 Apr 2024 01:39:14 GMT  
		Size: 31.3 KB (31343 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:2d8e91d5fc563dc929845616703196ec9f85778722f4bc8de7d72d893a503d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121273282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438408563c562ca1902732f907a14c198d803b0d0bb5662a6864821f53ef9c72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cef15f6c363a6f2e9b2d92afeec3cb9f5af90b8aa4610c70659666d58bad6`  
		Last Modified: Thu, 02 May 2024 04:08:34 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61166271eb59d611fb52e2b40a2ffd6d6e9af7e3a5ac80b05b62ef600cb642b`  
		Last Modified: Thu, 02 May 2024 04:08:33 GMT  
		Size: 5.5 MB (5531992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0cf7f7166b23e87380c7baae6dc23b031416490050fc05406de6ae29eb1a9`  
		Last Modified: Thu, 02 May 2024 04:08:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468402414545d5100eb103fe60e61dd53038299fa7bb9d616c4f0c159e876db`  
		Last Modified: Thu, 02 May 2024 04:31:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2d9687a58449d8d0eff4eee0e8fbd99de0f0e9513bde6459b91adc8de2cc5`  
		Last Modified: Thu, 02 May 2024 04:31:50 GMT  
		Size: 87.7 MB (87726852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfbb2500669cd0f0f39de01314f5b59e7943d9f46d98a1b40518f373fbceb35`  
		Last Modified: Thu, 02 May 2024 04:31:47 GMT  
		Size: 3.6 KB (3604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badb775977b1e5a3e709f43c8d379d190e4a54a1f4a9e789e634c3a6bd967604`  
		Last Modified: Thu, 02 May 2024 04:31:47 GMT  
		Size: 8.2 KB (8241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:5d59b105e71af4fe38c90379c67f27cfca041f89c6f2ffdf946339d1ecc329bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4585956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bc21215adbcade401d09e2c9bf0c7313461bbefaacf7f23b350a7de89beb2e`

```dockerfile
```

-	Layers:
	-	`sha256:8733e1a4f16a64d3c650b7d9135590c5ea42d6eda6614793c655d807f0d42d30`  
		Last Modified: Thu, 02 May 2024 04:31:48 GMT  
		Size: 4.6 MB (4554683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9806f008902614f8602d220986069fc990e052ed0470a28bb93c09a4d8545e6f`  
		Last Modified: Thu, 02 May 2024 04:31:48 GMT  
		Size: 31.3 KB (31273 bytes)  
		MIME: application/vnd.in-toto+json
