## `mariadb:noble`

```console
$ docker pull mariadb@sha256:b96d369c3b1bcd969f0a84f841771a15d722a231f7f49fed98ff1c515bb882a1
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

### `mariadb:noble` - unknown; unknown

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

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4a4b43bc5ffe5796cbf00614d7bb04f8116b9ed9038eb2379ae6e2c8be03eeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122809877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34094fbe018c533b1efadb480d6ab164d8e6001005f1ed7debfda518e004f961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c797b96da6d6aea3b8d371addc5cc9909f4c92777b0f712763eec4bbd02830a`  
		Last Modified: Tue, 17 Sep 2024 02:23:52 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71864f0bcd92d33d88272c953b6d5d3867f8e549cd62359c8f0e2d7a2386579`  
		Last Modified: Tue, 17 Sep 2024 02:23:53 GMT  
		Size: 7.4 MB (7350609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9934a3f3760abad967627bd554e94954ab1097fdf6525ab78e49e506e59cc`  
		Last Modified: Tue, 17 Sep 2024 02:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ec65f920a373f74d87260f3b08986b217850e92101e65b11865fd48b1a515c`  
		Last Modified: Tue, 17 Sep 2024 02:25:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08200f5baec1f9fc6b3d8a6d03732839dd937d2a0fc03a6905d974088253446`  
		Last Modified: Tue, 17 Sep 2024 02:25:44 GMT  
		Size: 86.6 MB (86559473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b33b922b8218974958036ed751414ae187d79bb79114a9f8305d807b3bf`  
		Last Modified: Tue, 17 Sep 2024 02:25:42 GMT  
		Size: 4.0 KB (3978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0698c26c2c354bcce18ef7217f4f713ace912115c4f7e5776134cc9f3c71447`  
		Last Modified: Tue, 17 Sep 2024 02:25:42 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:2cee1b229c376a3a81211d68ad1fab2a9e735363f9be918d620e1b14ef597d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4101187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c10c210ff3f6ad9fbdea076ee72ef69d8dba8b01aaa3c3388b75726581b8779`

```dockerfile
```

-	Layers:
	-	`sha256:b35c4c3caaa6a23feef12a93a88208e6e0e65090c071b62584802a98687c2a10`  
		Last Modified: Tue, 17 Sep 2024 02:25:42 GMT  
		Size: 4.1 MB (4069864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a7cfddb28f2db95da26e7ff3651215e1396f5f6a2665a612e289b04b2e6b5e`  
		Last Modified: Tue, 17 Sep 2024 02:25:41 GMT  
		Size: 31.3 KB (31323 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:64cc5a15a31e5cccdfbf8d772a04b967f1db327307fedb5db9c4e3e1c7c10ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133269159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d340c24eef3dacb89e67c49965fb8df5616129c09a83f5cb5285dd13908ced09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 03 Sep 2024 02:32:52 GMT
ARG RELEASE
# Tue, 03 Sep 2024 02:32:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Sep 2024 02:32:52 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Tue, 03 Sep 2024 02:32:52 GMT
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
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d156a25dded4a88503f9111433e1ba5f0f3abafbb0cd347ce7f044c0ade038`  
		Last Modified: Wed, 02 Oct 2024 02:32:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6296d73ea5a7b6fae7d1da14ee4f139ffbdecac54e9d08a759e90a69d813b200`  
		Last Modified: Wed, 02 Oct 2024 02:32:50 GMT  
		Size: 5.9 MB (5937002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7312677bf3ea598e3698664b3a4dd0f91efd90f0943aa34be187154e3736a1`  
		Last Modified: Wed, 02 Oct 2024 02:32:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03243e939c3e072b4f0f57443f4a1068e46b2f1ad5b30bc9cab49793fb40ede1`  
		Last Modified: Wed, 02 Oct 2024 02:34:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337bc081d5349fc7f1e5a1b4642e3ec576d1f46379cea5242f61b691d536fafb`  
		Last Modified: Wed, 02 Oct 2024 02:34:06 GMT  
		Size: 92.9 MB (92925942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bff42e489928ef9bef842cb9ff53d04ed3476a4f599f22eb6f8a0c2caa9690`  
		Last Modified: Wed, 02 Oct 2024 02:34:03 GMT  
		Size: 4.0 KB (3979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0b24a53f14a294ec32dffcdc4e1cb15677822c30712046bba02e2186964454`  
		Last Modified: Wed, 02 Oct 2024 02:34:03 GMT  
		Size: 8.4 KB (8424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:5d0c48865b3692488b1c1d867ebe28740d86c4c4624966a0110f2e626ef9a068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4101395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ed7ce88adb4b4d83e35ea9c09a589e0b843bdbff4a5c46cc247242bf7ad9c2`

```dockerfile
```

-	Layers:
	-	`sha256:ee2cd28a859f13f82480202e342a380811937464f0de83242a3471cba0e6f408`  
		Last Modified: Wed, 02 Oct 2024 02:34:04 GMT  
		Size: 4.1 MB (4070346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd9e68e82ca2a3cc42225a08d86ea28d925f7355bc009d0b14755704b09d7b3`  
		Last Modified: Wed, 02 Oct 2024 02:34:03 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:460623a2c0fd7b68812f923563567cce7005d3ceb625fbf50b76ee0539efe810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129407594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfcc75d53463ce3402308e5f21b8aeb40cd095b1b4e3f5af4a73e297fac711a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 03 Sep 2024 02:32:52 GMT
ARG RELEASE
# Tue, 03 Sep 2024 02:32:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Sep 2024 02:32:52 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Sep 2024 02:32:52 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Tue, 03 Sep 2024 02:32:52 GMT
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
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead35b8a4f97493602a2f9c3ffb7951652431c7a6e1dbbc9f8ffc8d0f619066d`  
		Last Modified: Wed, 02 Oct 2024 02:22:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe96948a8dcb573e73cb46da1d9f6b484461c977cf4f01ddd6a47a49fb6e25e`  
		Last Modified: Wed, 02 Oct 2024 02:22:28 GMT  
		Size: 5.5 MB (5507087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270b5596f460fbde29e240ea8e74dc88f602fa8b7fcdc2756b5340d3624969b1`  
		Last Modified: Wed, 02 Oct 2024 02:22:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bfe014ead40652c9db2c834bd35299ebb0bd21154e666017b34ff83116c3fc`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940e04ef19f81cb297a682f5c6c57e6ec7b22e3a1e4052a22db4e0e36fba39c7`  
		Last Modified: Wed, 02 Oct 2024 02:23:38 GMT  
		Size: 93.9 MB (93861695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ac91124b4f479faace013547287ed7c0702e115d813cb90bc05f297097a25`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 4.0 KB (3980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f4faf810d2ba5f8bdc6ba14d1ca83a30df9d06ba45c4c4b658661335ce667`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 8.4 KB (8428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:17ce2d31bd51b1b50db572ed27509960f828d0722fbef18f8dd11714f18dfda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4095305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56581eb5cce5b8a63a911fd009a89fe35dd15a3af2b2f625fbd4c4927b1aaa39`

```dockerfile
```

-	Layers:
	-	`sha256:92347d1a812438af2fa94ff5f278143767db06400e918266f0539be3af24e9a4`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 4.1 MB (4064326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836fb9650a89677ecc63eb59114afdb7975097af2ac664b5a452d4339a8535a3`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 31.0 KB (30979 bytes)  
		MIME: application/vnd.in-toto+json
