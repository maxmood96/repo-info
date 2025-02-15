## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:3944dd24218a6612521765bcc4c681e633e2399ad90c21b1ce42528014cdd01a
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
$ docker pull mariadb@sha256:78baf14fc64065e56fda25fb5abd1d200a2a2375392de0f0196fd49084c073ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107406119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a914eff5d2eb4c650a4e787e453d52a4ffba977632bd624cc6e63d0c9c4c2d65`
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
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdecd990c29c08034e51ef18a621e277e08aed24938ab2ce2bec9e957afa13e3`  
		Last Modified: Sat, 15 Feb 2025 01:35:33 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db80086e4da9be830eb658f825da35b3b091168697dd7c0dac44c810b3c4355`  
		Last Modified: Sat, 15 Feb 2025 01:35:34 GMT  
		Size: 5.3 MB (5346277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901fe9394c0053c71c4673bd837e46d8130171e15bcd28dc8903dc09ee0a7e6d`  
		Last Modified: Sat, 15 Feb 2025 01:35:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb19e1b10287ae658dc4f326b2530c3450541d399e8a02c48c0bd7ba536f9f`  
		Last Modified: Sat, 15 Feb 2025 01:35:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597f7afe50fe00b7cd3c898926ab5215536fe75ceff69cbcdeb5a66ca6ebd505`  
		Last Modified: Sat, 15 Feb 2025 01:35:37 GMT  
		Size: 72.3 MB (72291324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dede558384100aa3813e2afe227b0c6c09a4c57242080e7607d980eea1858d`  
		Last Modified: Sat, 15 Feb 2025 01:35:34 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3a22df929bad697d0a1639c04634446f1a92b4a2c611c4542b356a02af9071`  
		Last Modified: Sat, 15 Feb 2025 01:35:34 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:bafd0c0913cd85cfaac4718c1d04d30fe2a657f3bf0be24071d9699f6789d4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0afbf912a46e0e4f8b73b7050b22e2779a6657838ef495d3aa227b3ed124246`

```dockerfile
```

-	Layers:
	-	`sha256:e632ff4d96dbe537b05b089729a2377c71942941c3144e4196aa5d21f4656bc1`  
		Last Modified: Sat, 15 Feb 2025 01:35:36 GMT  
		Size: 4.1 MB (4083786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6f1c5c2d10fcc1c7b5b8a2809c02da718c17e45f22707193419f8c12726bcc`  
		Last Modified: Sat, 15 Feb 2025 01:35:37 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4625319477deae59b24db70563e2d00e141e68f0b5910210bef5c99d1249bc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122858829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d045ae11ce7ea8529ff420da5b7f4f19302c0824db2b81be3fed1a2ca8c4e639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
ARG RELEASE
# Thu, 21 Nov 2024 21:43:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Nov 2024 21:43:46 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV LANG=C.UTF-8
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab783a6a145e4df87e21cba35410a1bd6cf746bb77533a349ca8ba9ffdd023`  
		Last Modified: Tue, 04 Feb 2025 10:52:38 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c334a5d1f6abe7dd3b554de12c4f0e2bf6ae1daa132c2556a7566a3a0ba1fe9`  
		Last Modified: Tue, 04 Feb 2025 13:36:40 GMT  
		Size: 5.1 MB (5126105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0626685d68c7a72072e6dea5a55900e40a0d8dedba5261adee4e391d5d3dead0`  
		Last Modified: Tue, 04 Feb 2025 11:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32ddb4a99155a7fd1a1d4f6d5ff9ab96b8b32dc1e19917bfb468ef94964178`  
		Last Modified: Tue, 04 Feb 2025 13:36:30 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d836d362405837f9321b716602404dc8f81b6b0fcee883e88bbb8eabb815532b`  
		Last Modified: Tue, 04 Feb 2025 13:36:34 GMT  
		Size: 88.8 MB (88824897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab43e8e60e366923cebd7448d02dd1dc5264335dadc12bfec2164ba119a6320`  
		Last Modified: Tue, 04 Feb 2025 13:36:17 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d56ae0de764759db6bc21fc4efd2ca89f0a9b9a0fee2a723738fa3d8e06a241`  
		Last Modified: Tue, 04 Feb 2025 11:48:11 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:a47d911e620e648fd65b274b2f6f4b505bbb68b4f41f26789f780a82756531eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75428b297367b39f63dcda17f4c19821309a59cf61879fa003af34e57734beda`

```dockerfile
```

-	Layers:
	-	`sha256:88aadf34fcd368a79b0d7553fef781a7196cd448d0ce26c011fbd4e6701591bb`  
		Last Modified: Tue, 04 Feb 2025 13:50:23 GMT  
		Size: 4.1 MB (4091055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb750b850da1f8119d6410b599e2d07e02c0b23be71ca68b448a42bbfba8536e`  
		Last Modified: Tue, 04 Feb 2025 13:50:23 GMT  
		Size: 31.4 KB (31440 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9bb66c89d5877da8abeccf7663f22b3c22ed18b96bd745fc6da3ff0f340c59d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cd863ce346ee025c33bc59e05cab9a6af7dd7b1d03bd67a4015bda28dbb425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
ARG RELEASE
# Thu, 21 Nov 2024 21:43:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Nov 2024 21:43:46 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV LANG=C.UTF-8
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d3281d5f611aa457350980753108fe328b1af4f31ec8ac610ebf3e087b819`  
		Last Modified: Tue, 04 Feb 2025 23:23:23 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9073709f8a9cd57bfcde784c6a4fcb9f36094f0bbd9bdf63d80a2b4f6b30a71e`  
		Last Modified: Tue, 04 Feb 2025 21:30:25 GMT  
		Size: 5.9 MB (5914185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a366827bcb88f16a1eed75bcd43b3cda70e45d8a5269a835ef7e006762231`  
		Last Modified: Tue, 04 Feb 2025 10:40:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b19b6a326142ff983008f798240caf127ef5d0f7afee8fa911ee41a8a40c259`  
		Last Modified: Tue, 04 Feb 2025 12:00:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9414c1b09595f9255dbc6137755dcbf809de7440e4d9c3d534e415c41e8838`  
		Last Modified: Wed, 05 Feb 2025 00:00:59 GMT  
		Size: 95.3 MB (95276903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d614571e1dc4baea047a4aa1f126bcbf5e035d0157015b32dc9b79200af87`  
		Last Modified: Tue, 04 Feb 2025 10:41:06 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6c1d97925e360187d995523f35e3417984d48b6272df9f77da39db32de6e2b`  
		Last Modified: Tue, 04 Feb 2025 11:00:59 GMT  
		Size: 8.4 KB (8403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6e66170bb9cca42ecf6b30d8614478a4b41fe336c4ebf955080cd90c72d4594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5946ea87812ab32696b6c9120f3c330602e71b6d655593add8449fedf510feb`

```dockerfile
```

-	Layers:
	-	`sha256:777f587ce77007eab6c4df50fd4339129e0fcc39ecb0672fe8d42eafc18c9231`  
		Last Modified: Tue, 04 Feb 2025 21:30:28 GMT  
		Size: 4.1 MB (4091535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2411b179b9788bc90b0916414c270adc49d13bc5bd90ad40de86254866591d4`  
		Last Modified: Tue, 04 Feb 2025 13:30:26 GMT  
		Size: 31.3 KB (31304 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:d34f3e27d62ea3ef5dcfe5e2c0391654c2c1dd8ca452cb21c2e9d6f11ffc7ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131820154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb17aee8d819e299ede0d6ed2d72a69f0e4bce3eeebd03b5a031d1da9ece7d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
ARG RELEASE
# Thu, 21 Nov 2024 21:43:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Nov 2024 21:43:46 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV LANG=C.UTF-8
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=1:11.6.2+maria~ubu2404
# Thu, 21 Nov 2024 21:43:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.6.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.6.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1789514f1b76a7b3e93f8f3cb02a2e551b610c2bcc279e97df0204b1df56f1`  
		Last Modified: Tue, 04 Feb 2025 10:50:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1f8c3404e74a12c5792781167247abac8fc149fe2ec3fcd2a0ce5a25201ec`  
		Last Modified: Tue, 04 Feb 2025 11:01:18 GMT  
		Size: 5.5 MB (5482974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26462072abd6964122db852882e7083129bbbc80945430682c782c3e42bc6302`  
		Last Modified: Tue, 04 Feb 2025 11:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14424c849cfe052ead514ec4c6304b1abb66e867d0269e824a352d3461b72e9e`  
		Last Modified: Tue, 04 Feb 2025 11:01:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310475dff09c673e8c771fa176a57f580afa4d35cff2ace5b9bc7f314cbdd7e2`  
		Last Modified: Tue, 04 Feb 2025 11:01:51 GMT  
		Size: 96.3 MB (96295386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f0bc6f523e0b55a3fe3bbc5809fa5c884fc58c8713c0e3db5bb06ae565ca6d`  
		Last Modified: Tue, 04 Feb 2025 14:05:46 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9d9b608c773649a3a31b6e7cb11f599733794bb37f34f6716e0c5d5638c884`  
		Last Modified: Tue, 04 Feb 2025 14:33:55 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:eeffaf70923fbfdd306cdffe9133fed489256d8e6056fbe8e415a059ce19879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73263b6576f3dde490384536892b1558f63c0a6039f421660b27c803763e7924`

```dockerfile
```

-	Layers:
	-	`sha256:3ef79d557e54cee3539aea863c85674e06363680d385e2e1520413bafc984118`  
		Last Modified: Tue, 04 Feb 2025 10:41:19 GMT  
		Size: 4.1 MB (4085505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba572f47e809bac5eff731855f933a080bb23c7aa8f17866da1576c6e98bde7c`  
		Last Modified: Tue, 04 Feb 2025 13:30:35 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json
