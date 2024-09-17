## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:a1744870dad0a8a8a5c37c6f0c9775ec9df0f7344a8bff96bfe24b291ae617f3
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

### `mariadb:11-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:7aed47d5c0e579fd2cd55878fb1d373bc7462f48f2831f57a889f6fb30c0497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125009176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f5b532c2efdda2ae735470b867b1ff0335a00d2af50577aedb15eb9f03de2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:32:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:32:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.5.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:32:52 GMT
ARG MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ENV MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:32:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:32:52 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:32:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e0d69d765cf53c4ab592ad6b91259a1b83b754d9c05503c4093a0d3bd12c0`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5145df719521d5ed2ba7fad41803f73cf6fbf5e09ce2a703f69433c10b2212fb`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 7.8 MB (7755615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe11d25f6eea92c1466527b53194073d9f7aeb8a836c97966f7fd03b6f0ac0e`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb027ac47e46d211a0d1728432291af7c947339b6d581c4cee23b5488f83b4`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586260156254c4e6d87732d4c11bcef796128755f6c3c7cba5bb528979df4981`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 87.5 MB (87489543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c80f8d2eea66f965a0c86c9ec7d08d445a435634ca45fa25feb6fdea0734f8`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 4.0 KB (3978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36be09cfdba3d9b36d3eea947fafbf3345d25fea4fea4aa54e8f6090e8b46a42`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:f087f12edd6488031a55519426101ff680ea09e002a18751e64db09df8bfc624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85d7fabcd8ce6473e39c568d7ad77d970ed3cd981af1fbd717e1e918fa66a6`

```dockerfile
```

-	Layers:
	-	`sha256:dd9b044ef2103782d6919c7f72414af87b8a4c72d5064fb3f9f294f752bf053e`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 4.1 MB (4062585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee7230e5a1be28c727744c6ac57f856a021dac3eee1b3ee1873ddce14a78fc6`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bec5218712da80452783351921ad6642734d4497b89555d3ab56e7fe88b5cc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120546192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6646f937d9e17a36fcef1e76203c3c6c7bfe443810b35788e4cddd34912162ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:32:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:32:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.5.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:32:52 GMT
ARG MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ENV MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:32:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:32:52 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:32:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3291cf9bba67c91822cecd3b5d419bcd936d852c4dc5aaff76a738e732e9b49`  
		Last Modified: Sat, 17 Aug 2024 03:10:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3969bcb710ce8552dea9c7e3618233b26b0c230eaab39c5156ff724dac851c`  
		Last Modified: Sat, 17 Aug 2024 03:10:17 GMT  
		Size: 5.1 MB (5129577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a948c6a0af0cb95e3f26ce3ba4e7832d8149d7d99eb58c32a79321f5a5c4ecdf`  
		Last Modified: Sat, 17 Aug 2024 03:10:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af3abb71490ff3f77797a11b7642443a6674d8d19082fb2b432272530cf94`  
		Last Modified: Sat, 17 Aug 2024 03:11:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88cdca10a21b49055f9fe0dbd752813b5ea81b1cfa43b8141ac3435980e47a1`  
		Last Modified: Sat, 17 Aug 2024 03:11:14 GMT  
		Size: 86.6 MB (86558742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6ec50e732275d1c855165ae49871ce09cfc76bcb810940f844a6daec8a843`  
		Last Modified: Tue, 03 Sep 2024 18:59:19 GMT  
		Size: 4.0 KB (3975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f7003768f2d993f31abeeac23c029a0963b73feeeb6812fd11affbead8ebc`  
		Last Modified: Tue, 03 Sep 2024 18:59:19 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:f74d6b2e1a75ad2d2f6b689333f5ed45558c5436efc8ed46980d244480963cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b0ddd1bb3942ff3c7287be2f8cefb1fa196134813bc90d4e04a0d42318d81d`

```dockerfile
```

-	Layers:
	-	`sha256:5a831437cc039ba533e39101c23f124ee8a6290540760af6e8d2d7ce6bb51af9`  
		Last Modified: Tue, 03 Sep 2024 18:59:20 GMT  
		Size: 4.1 MB (4067314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477e99639f1d4380819887504d2679ae2ad906ea44764133e7a06cd3cf6348df`  
		Last Modified: Tue, 03 Sep 2024 18:59:19 GMT  
		Size: 31.3 KB (31323 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:09ef2a8f7bf4f9fbdc10c1f1d3231b8c18d3042afef3c380fd98249e91066b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135895817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352fd17daf4b754f4cf2b704a285eef61a9fdda42e630eff438962e8375f15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:32:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:32:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.5.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:32:52 GMT
ARG MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ENV MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:32:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:32:52 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:32:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acf3d3aea23d3ca827d3c9c02b6bbceefd98b17cd3b5d74128e605f9a4bbd8a`  
		Last Modified: Tue, 17 Sep 2024 01:37:05 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1909086bf4104f7007c5f7c0be887fb573b5554ea0ee0293fb9c4d2ff50ab5`  
		Last Modified: Tue, 17 Sep 2024 01:37:06 GMT  
		Size: 8.6 MB (8563087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d1f5fa1bfae1678bdabf19ec94a6e15241630591de537b6c6c3ff46a461ea`  
		Last Modified: Tue, 17 Sep 2024 01:37:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4528b63564ae5fbd6f831875969e36e5caa94714e2f0ca1c005a42a6d10c8aa5`  
		Last Modified: Tue, 17 Sep 2024 01:38:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f23f81c58b7361534d027d3782bf75a5fb96a7002531f56fd05c953610e8c0e`  
		Last Modified: Tue, 17 Sep 2024 01:38:32 GMT  
		Size: 92.9 MB (92926188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58105f6f5abbc6bb33da145c6b390b5dca7e9d996ba46d7df9f55c9fa5aff8b`  
		Last Modified: Tue, 17 Sep 2024 01:38:29 GMT  
		Size: 4.0 KB (3977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07552f3b4c2737863d2184593a1f04ca84ab8a9257c66adf5948909e354d669c`  
		Last Modified: Tue, 17 Sep 2024 01:38:29 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:d90bfcf4b9fef89dabdd6c6fe694f63867a3ec519546bd3dbeb8fe320857c783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4101377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db77645714270c984611dfebfeccae67fd1f79512239299a61a2df113decd19`

```dockerfile
```

-	Layers:
	-	`sha256:18a185f52193b2f4ead7b86492006a4957a6f924be853e8aa0a92e88c825c5bd`  
		Last Modified: Tue, 17 Sep 2024 01:38:29 GMT  
		Size: 4.1 MB (4070333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593ca94d6c91e434ada37e0613f7dfca1fb1ac18dac5e2fa0cc29fc49571a9be`  
		Last Modified: Tue, 17 Sep 2024 01:38:28 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:a666986036c67a649ff1cbfa93fe006bc81acecfcf1cc6efd4e5c18a236f536b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131500664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7bcd0faa592080f4254e980bffa145ef1d58c13a867e138f0d4f5416d0e54a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:32:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:32:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.5.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:32:52 GMT
ARG MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ENV MARIADB_VERSION=1:11.5.2+maria~ubu2404
# Tue, 03 Sep 2024 02:32:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.5.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.5.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:32:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:32:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:32:52 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:32:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:43b981c5954bdfa7626a4bec06cf075f7bb2df6698b5c0b42b5b5770109637c6`  
		Last Modified: Tue, 27 Aug 2024 17:08:36 GMT  
		Size: 30.0 MB (30024629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712ca6f3873c2145d1a291b0d408a68add66fd54ae0a978612a1c3562c8e17e`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e5b99e7ca48946c95b0839303199b77c809240d369b1c44d6bef242276016c`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 7.6 MB (7599715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce2b4ac53e38de73d1f4dd5b15c3bfe0383e1338bbd31b3db09535d4095eae`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c0f402f3f9a8549bf4e810d78f86e84552bf6288194656272a4561c3b492c`  
		Last Modified: Tue, 17 Sep 2024 02:18:09 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60600d3eee31ffa50489f7296ea687bc10daae6994a465039a8c9eef5d48ab62`  
		Last Modified: Tue, 17 Sep 2024 02:18:11 GMT  
		Size: 93.9 MB (93862120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e79b54d56cc46eb7b01f47f98ad78581f04b0b7d2fd2df308db00dbe2073c2`  
		Last Modified: Tue, 17 Sep 2024 02:18:09 GMT  
		Size: 4.0 KB (3980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf75c09defaee37af6d365763becbb97e75702d23e0ab20f058f7921201466`  
		Last Modified: Tue, 17 Sep 2024 02:18:09 GMT  
		Size: 8.4 KB (8428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:123d925cf540cf34b9a2dc0bc44ac7e307d62f006499081991eae4e2d881953b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4095287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f477946223bc4d04c089aeb50eefb7a8252a536f8e87d1175fc34e3d420584e`

```dockerfile
```

-	Layers:
	-	`sha256:c74e99186dee2409125b7a6bcf80e27475a6d317d18483694241b457204aa415`  
		Last Modified: Tue, 17 Sep 2024 02:18:09 GMT  
		Size: 4.1 MB (4064313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5c1b7f3f6bbbc1a1c678c20e45bbaab25bd7dfd87fb01cb5805c5b31eeb960`  
		Last Modified: Tue, 17 Sep 2024 02:18:09 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
