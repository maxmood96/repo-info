## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:5dfb3093333fa0ea53194ddef0a2bfa21d3b1e1353bd228b22610cd6fc0c04da
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

### `mariadb:lts-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:8f0b045968f437f4a8dabd5f66fbe81472ebb0f2473e567819485427654a8e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106926427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bedc5cb9292f8b3b97b8325ae671d63b9ff4e5c4216affbbdb04da552791b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV LANG=C.UTF-8
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00540d4e3eef7c831ffe1f7d6d38e36ccfba434a05838a63d224e44056ba98b`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae521746ca6f01da8a44743f440b079b1486ddaf8d0bc8ef637d96d5db892b6`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 5.3 MB (5346302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053811f9b34ff4df8547e4897ed67cdb1b8a4c045b612e29e0d3c6194b3e6ea8`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd00e0e9fda4b4cb7147ac7e2c8972bfe0a15d54fc44a258bd0d0d96f5a6a1c2`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862d4624453e3fb23eb1e362d527e01d2893910b92d730ad32442ba9d6b99f6b`  
		Last Modified: Thu, 06 Feb 2025 00:27:02 GMT  
		Size: 71.8 MB (71811611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f308c68bfb3b588e489a7395d59c3fa9765931bc04d52e536bb50e46effe0b7`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315019d0e7c464d6ab5b0f2359cb1424ffc266806d86c39529627cc1be84735d`  
		Last Modified: Thu, 06 Feb 2025 00:27:02 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:cda5c3e333b261a9d8be323855a9319397f62139375a8fdec58a40fc2a1d0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6167f4cf0827b51a0c37f7e9d3aba0b5516c36ae14da26b68352a7a8117df24c`

```dockerfile
```

-	Layers:
	-	`sha256:0c3a2bc78fcdb3a1312845e22b978c1ead9499ca150101d4e11f1b4cca87f8a9`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 4.1 MB (4081596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0328a63031b9dfa4ed706988c372235e82ecc133e40ac0193274b7055b178a51`  
		Last Modified: Thu, 06 Feb 2025 00:27:01 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1826a95f2833ef65476256ee360994dc2940097317356f436727aa07a2c0b538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104886813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854d14c603784987e80c678430e87d4b42f185836bfd3c89eca17dadf89ba2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV LANG=C.UTF-8
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ef5d89f367d315c3805024fcb4763a5f528749dae6436979669a9fd85d4818`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200533c6762909d53b17a0615f8acf60a19b610c8276859a3db5cf0aa522d380`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 5.1 MB (5126430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6dd593aefbba5d4c6adec89d83647d7714dfb52be2378f788074e85f6e4af8`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c280eba0879f99bcad006dc95245d78e47e639e11b373b53d34154a86914e1`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c8ee39d86fccf283cf92ecfedc5ba49e56e1d3ea4def059dbf43b7024815f`  
		Last Modified: Thu, 06 Feb 2025 00:32:50 GMT  
		Size: 70.9 MB (70852562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc19b37ed75095e5be618d305e765f3efa0a506f9ff89370fe0279d549ad83`  
		Last Modified: Thu, 06 Feb 2025 00:32:48 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa71363d3f7c3b12a2fd9351a8517bcabb2646c4cb33985d855112703f0897b`  
		Last Modified: Thu, 06 Feb 2025 00:32:48 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:1d7652472326d8fc2817907908e1a1d33b32ad97a5a941ea504524496e071ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7605da963022611c66e930dc55fe13ac93f057141b53d657b3e3cd480815d87`

```dockerfile
```

-	Layers:
	-	`sha256:ec1da2c81d7c60cb8fc10f1921178b3b459709f8f9e0a26124f9d873ed301e48`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 4.1 MB (4088844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bb009f1619ec8ca18d7be4943f544da7ffd339002329c0a7226fddd726af84`  
		Last Modified: Thu, 06 Feb 2025 00:32:47 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7039b39db4a692e2893481ad1c7f33ff27e0c18f1db50749ee0e350ace5fd83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117177307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727be29dfeadb78f7d7b047f4e3b3003cebc25bee0629443cad716c84f3bb89c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV LANG=C.UTF-8
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bb389496bb9ad44a6b311b2cc7702ece7d85a2d524801ed69c0daa82b88f92`  
		Last Modified: Thu, 06 Feb 2025 00:48:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232eb481c0195bd31092a70e08d5de6c9a3e59ea4f24fbfff2e46b5ede78cceb`  
		Last Modified: Thu, 06 Feb 2025 00:48:07 GMT  
		Size: 5.9 MB (5914651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374606b46c050b8b7b0b53a6619aedd834eb7383cba72969c5587c483c0c4c8`  
		Last Modified: Thu, 06 Feb 2025 00:48:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d52058771902100b40c3d44dd3a41c83562847444a550132f09c205dd54663`  
		Last Modified: Thu, 06 Feb 2025 00:48:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e84b2457217276d5e966da787254010efffde2f7892c3f860e95f028623443c`  
		Last Modified: Thu, 06 Feb 2025 00:48:10 GMT  
		Size: 76.9 MB (76858602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c151312efd1be34ff286dad5447d681dce716638cf8057122e8cfb78dd0b6e`  
		Last Modified: Thu, 06 Feb 2025 00:48:07 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c631d2652a260c53f903a15d283b1f4fea829be01a1d28821dd795fa81335130`  
		Last Modified: Thu, 06 Feb 2025 00:48:07 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:bc2ec6a462e40d8fe3139f043ae0627ad92ead2a94ed383284d29175726124fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1fc26478afaeea48c5fdecdf56964bbcce8ca40c1e877d3e158f4cbfef75e4`

```dockerfile
```

-	Layers:
	-	`sha256:0b65a1d7bb8eb2377b40d849761cc4a3c48fda95ba3d5e1b0dd87e8074abb8c7`  
		Last Modified: Thu, 06 Feb 2025 00:48:07 GMT  
		Size: 4.1 MB (4089332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d99035e60fc4c18a739af261bba3305446bd476f23f7e6d8c8155c6b4413b9a`  
		Last Modified: Thu, 06 Feb 2025 00:48:06 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:4ed4a0521394679246c7d8fd3c322e3a65d68f04c4f84da03db8d2c6ffa319cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112408093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577a7c0ed92f3892198baefc2632c9381db458a3d7a9159c8b7a33512dcad37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV LANG=C.UTF-8
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=1:11.4.5+maria~ubu2404
# Wed, 05 Feb 2025 21:06:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.5+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.5/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9aa34f263132852301404d6c5d459e61f3e37eac2a53a00b647f1b2b87210`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998b7c2fb3b9d7870eff6bd3ee89ecc02630300a0fe1ab0cd76c769e98bd32fe`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 5.5 MB (5483331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a520a479b4a41ce07b471ce1edf3160c6f00df96441a64a82c4b9fe7325a901f`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb44a0005a8cd69c4e547de6628a42263dc40dd491b421db763039b6a8435048`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f951a98088f1039386d47e9e30d436ec32692ff1180c7366d17a399f5ab79757`  
		Last Modified: Thu, 06 Feb 2025 00:45:55 GMT  
		Size: 76.9 MB (76882967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba37274bce89f6fce3a35519ad6dea080c9a32433327b69d44f1758155da6cd3`  
		Last Modified: Thu, 06 Feb 2025 00:45:54 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24534a792dcac9d54b70d446c573a7c96ffb20c4f9c86dd1c93c93d390b0f161`  
		Last Modified: Thu, 06 Feb 2025 00:45:54 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:0c81687430e30a4f812be2093342675197929eb8df923a696416dadfb838ccab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b397ad14cfa537b87cf7e17ca0c01174ffa1d878b4db0c9510c997edeeb802`

```dockerfile
```

-	Layers:
	-	`sha256:68c5fc81687823fc461c83917d7c56c8f7bad24a2f88c86d78d66864aaa262a8`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 4.1 MB (4083320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5531c596d29051f93ef7e01f9c4ef8cccd2da353c82314ef0e8a32ae647ecb8`  
		Last Modified: Thu, 06 Feb 2025 00:45:53 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.in-toto+json
