## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:86bf3ea9ba309bd81eecdc1cd9f54b49ea42e93bf2750d615230756520ea4b9f
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
$ docker pull mariadb@sha256:b933188ca9396bec95b299cf1a58ce1c43086a861e79d8a670a10b569c50d453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105369137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406d3edaa4606a942a5b087f560e2a5463f6e2787aca49193da67031315fc09b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d06c66f8984450e77f899e6ea9fb6b43aa1299c0e9bbf4f1c7c57e34d7187a`  
		Last Modified: Tue, 02 Sep 2025 00:24:03 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427991e2f34b98f5f78432d1d1d3e6db085e1eb896e479a266529767e73c5cc`  
		Last Modified: Tue, 02 Sep 2025 00:24:40 GMT  
		Size: 5.7 MB (5659824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37470673b781d4e84b7a6d44c3130fe3754a3af9dc258fa644671a37ed6d40f`  
		Last Modified: Tue, 02 Sep 2025 00:24:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197601ade724ec176a1d072ec677b9a2379163f426d32f38f61b6a5a3cfbed3`  
		Last Modified: Tue, 02 Sep 2025 00:24:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb464ad4e0ab67e62055657d26d180134a9b132a04e5f0a9bcdf69df705e067`  
		Last Modified: Tue, 02 Sep 2025 00:25:05 GMT  
		Size: 70.2 MB (70157819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c286c50b3b599a0e776ead42ce781a5fa563c766bb95b923a407553320f50c`  
		Last Modified: Tue, 02 Sep 2025 00:24:39 GMT  
		Size: 4.0 KB (4021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19683e685d4874878155d6edfcfe9625787675b24efa5ce09e1ba6be89fd2df8`  
		Last Modified: Tue, 02 Sep 2025 00:24:39 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3c77e5e8a40ed02ba75fd771c78c2207910f4d6ade13d4ae5fb8e81e42abb082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54747da4ba9e94851dcedb8572b47561a17cbca2f6d2c5a12d71baf58df6cd6a`

```dockerfile
```

-	Layers:
	-	`sha256:68fbddb4ac43d4d0ee2733c6a49ee631bb7659368ede42d107c894128d222aa7`  
		Last Modified: Tue, 02 Sep 2025 00:35:23 GMT  
		Size: 4.8 MB (4792974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a000d063c68480df92a3c2c001f3cff96235db0bb909c292be70359a91ce1354`  
		Last Modified: Tue, 02 Sep 2025 00:35:24 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:43fbf94a6f3ed04f04174ac0ece9f7486cbb3763a1dc8275d5ea315efd282b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99775375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6a410b3e5af3fbc578f92d293b9931a8d4b8b2cba96147c62f72054080baac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65368cd588932b13e2740f80c15aaa317771d60b7f462795848a7408ea55b9b`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dca71b612062a76e088ecf5d33e7e4cbd4e61c30bc9d85d534edd8e680ce9c3`  
		Last Modified: Thu, 02 Oct 2025 01:26:57 GMT  
		Size: 5.5 MB (5472223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765a5e39e40ea0624a4013f8c593c958f5d618c0e708090d17f85512051ecb22`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4225723d53b0a069cfcdfe17aedd2ff08307acd5a3366f9dc81c1b8be360a10c`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8e29ba3d6c8e59ebf9d286350f26c004ae018800099436ad39ed464ac4de97`  
		Last Modified: Thu, 02 Oct 2025 01:27:03 GMT  
		Size: 66.9 MB (66905490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a6ecf492c1c8e4ef0a59d0ee7c79963dd6b680493e55e1ca47a2fbc9e1b772`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec04f999abde87d9c76049b5a566080884e1ef065100b48e9545f9f3dbbaab1`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:c17f824f21316d844fab6b20c57968c9ab3434c347fbf2342297295019326a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4830291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4f64eee2216bf82ec91a4f6b7623a4abc3d6bfba7dfc29979a795eed1dcbea`

```dockerfile
```

-	Layers:
	-	`sha256:6ba8869f5ad70dfe6f9bb9e655718df3058d764a146ee3c8d2a4e8045f6f28ea`  
		Last Modified: Thu, 02 Oct 2025 03:35:30 GMT  
		Size: 4.8 MB (4799410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ab9aa6d43f1171e88bc516d62fe6074b7b618fd3fd1744cfbf45ca72a0d9b7`  
		Last Modified: Thu, 02 Oct 2025 03:35:31 GMT  
		Size: 30.9 KB (30881 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:84c2bba9bfbc753d9a83b9d8b60cee659d2de1fd80d4d9fac157bb297023b279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113007445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05426a570e417358c56ca88ce00198df3153cf0a4450c6adde7a719efa7a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4a7e837414a630c9c20b5d705de0bf0be24494257caf0ca7c158c711c7a152`  
		Last Modified: Thu, 02 Oct 2025 03:04:31 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadddd92daf4f98fe35921dfbcb73bd79cfb0d0e188b2b89d2a530f18beecd9b`  
		Last Modified: Thu, 02 Oct 2025 03:04:32 GMT  
		Size: 6.1 MB (6086469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e91c532babd13b8bb0efa0f1deb17b9e4d00ffc268231864558eb3b2c0360ee`  
		Last Modified: Thu, 02 Oct 2025 03:04:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c370ff147fea5aff7be72ac5a79513545584a85f2178bf418b7d33d7331bef`  
		Last Modified: Thu, 02 Oct 2025 03:04:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c8b7b3eb23883b10b2178e54ff7ab4957312cc01123d68a33776f9a2d4c9`  
		Last Modified: Thu, 02 Oct 2025 03:04:37 GMT  
		Size: 72.5 MB (72459638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3877ff1bc90287b1ccb1684713793f636c8a4222c287d68a3718e885b98fff2`  
		Last Modified: Thu, 02 Oct 2025 03:04:32 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891324d7a23adcfe2acb5d0f56dcd3f844924f0b3bb04e0a666727b161ce9b74`  
		Last Modified: Thu, 02 Oct 2025 03:04:31 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a874a3fdcafa27dd7846470cde93822de6c67980f4caba132123d04295c87b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4831524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545cdde9ccae74a38412015627248230fbc091b245ecd3853f76bb02294bc937`

```dockerfile
```

-	Layers:
	-	`sha256:17453c9470f145b2cfd9bba66f15811075b0a97533d11834f9183c4ca740db05`  
		Last Modified: Thu, 02 Oct 2025 03:35:35 GMT  
		Size: 4.8 MB (4800768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41697c92dcb6bc6243b3a2ba34b1d1476a53d233ad6d782dfd35fad9bc15197`  
		Last Modified: Thu, 02 Oct 2025 03:35:37 GMT  
		Size: 30.8 KB (30756 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:d7201acb24f72eb988fdc9bd6ea3ed4010bab38bd2c9a97504c8d9b308f27967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103196758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd1f33eb4966052ff905c2adfcbd63cd69a95db99b08cc0d154a42c1e055ccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4211311c107dc97b7f71a20a6425751735e3d279581d168dcb2f952069a5a3`  
		Last Modified: Thu, 02 Oct 2025 02:11:08 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fe48b79c05c02585bb8228c36b9a91ab78d55d2350b9d03ed9a53e146c6b1e`  
		Last Modified: Thu, 02 Oct 2025 02:11:10 GMT  
		Size: 5.5 MB (5541870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127eb04e08c39d97e2d2d282ab6b302f0911fcb9db535714c276e8adf6f2b1ff`  
		Last Modified: Thu, 02 Oct 2025 02:11:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff33f1c878e8a391af3fb859e18244785576b80e23ae9ffdaad53ff71ed94914`  
		Last Modified: Thu, 02 Oct 2025 02:11:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189575430347abbdba1118afd8bf220e18425b8de0d070d397021453d232921`  
		Last Modified: Thu, 02 Oct 2025 02:11:21 GMT  
		Size: 69.6 MB (69636928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1d6576187647ae284e43342981a4b41501dfdf4c04718a1796bd6c60cc824b`  
		Last Modified: Thu, 02 Oct 2025 02:11:08 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f2c136b907da47018a72f2bd2fd2560a5c8c05ec675c44a6e8bafd644e036a`  
		Last Modified: Thu, 02 Oct 2025 02:11:08 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:e29c4a073e0a717e12dc800223ca9c3c9a1549687bb85a1e4fb5b03fe7241711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef73df3196fd299890be00adb87887f2efb7a6c6d346f2ef4e011d527456cb7b`

```dockerfile
```

-	Layers:
	-	`sha256:8cdbb1e96c5fcf5f5440b06065b0a3b4e78410135f9d2800a1d2ecc312b2962b`  
		Last Modified: Thu, 02 Oct 2025 03:35:41 GMT  
		Size: 4.8 MB (4793299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646554ee303ed6f4ff49af032d0fd45a0cf06b05d6f5822a3873cfaaf4edaac5`  
		Last Modified: Thu, 02 Oct 2025 03:35:42 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json
