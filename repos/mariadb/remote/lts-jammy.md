## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:3ad5e75e58f135d0f4e59736ef504e6df5d1c347f54b99429f1af4493f3dbe1b
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
$ docker pull mariadb@sha256:e0a092f10ea8a4c33e88b790606b68dab3d00e6b1ef417f6f5d8e825574e1fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122467104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6f6d8eea0a2eec13955e15aa31621d341df5a90d1b9895da870b964e4aa3e8`
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
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
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
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d8e1823c6f7468067cbe6195cb8196beff8f8e5caaa95c91118ea9963b558b`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2e2edb76da72731afb6f7d9a3bca04e906d0add57ab5ac25a5c03954b1163`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 5.6 MB (5647189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df97d18a516acf3fb2bd191623581156b323db67cb02cfccdf2057cf660f59e`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fe851833067119510a2d340be72adebb6866e9d5e47c893d32d97ebfe462e1`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b891b67a5cf8cf31519411d0e2e43b9c9d099f3761ffb571b8bab420f9a201c2`  
		Last Modified: Wed, 06 Mar 2024 02:56:31 GMT  
		Size: 87.3 MB (87266925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d0cb433aa38eae144536defcc84ec82e2002ece4ab469df533fb714c10f5b`  
		Last Modified: Wed, 06 Mar 2024 02:56:30 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29a5135f8323299923efeccb2d9c8f9af0a99714b240412d0956fa9f4aacdba`  
		Last Modified: Wed, 06 Mar 2024 02:56:30 GMT  
		Size: 8.3 KB (8252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:8bb3b11b7a3dd9eaac874a6a7b24673561530aa7d0e0989bb0ddb7f4b553c161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4609101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9995697a97a97b5a3961315f686ff0ffda0b237ec54da5a308f001fabd3703a`

```dockerfile
```

-	Layers:
	-	`sha256:4fd54be7881f7e8e644aeeae1371ff715a0cea695780180a1b929c31917031b2`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 4.6 MB (4577671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b51683b70bed344897c327aa6be1a663a4c75f1bf4ef4ad7fac57c0d0688948`  
		Last Modified: Wed, 06 Mar 2024 02:56:29 GMT  
		Size: 31.4 KB (31430 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d8f82a56cec5a204e3b0663e3600ef3d58338f93eb07e5838c4cca91a94f449c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116866213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b0799a01276c9bae9c310930fec780bd0c0820ae5ec9d560e40bc1508d28f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
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
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9fa9deb29a6e3d9f25fc4957c625c64d7ec05878a7afb62fcbdeeeed6f69a9`  
		Last Modified: Fri, 16 Feb 2024 18:59:48 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d846006199d6124c3c214b0f3e23489d2043b955c1782f22b6ef911188c36a46`  
		Last Modified: Fri, 16 Feb 2024 18:59:48 GMT  
		Size: 5.5 MB (5463216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e3d3eb6f5f46effc5c13a2ddc7ba08d680ec0e2a55ae7bcacffeff1fd522ee`  
		Last Modified: Fri, 16 Feb 2024 18:59:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dc6b5c51d48190508dec7294e3b66d5af24a20e727b5c61bdee2b4eb7a7c94`  
		Last Modified: Fri, 16 Feb 2024 19:01:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694eb98596e79fd8c7178e2e8da5b587d677d18e6a1f2d971a4a39d526ab6c60`  
		Last Modified: Thu, 22 Feb 2024 01:55:57 GMT  
		Size: 84.0 MB (84032083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8cf47553b64444db1f5c24116ece57858b42c17722e28410d6ddd6bdc708a4`  
		Last Modified: Thu, 22 Feb 2024 01:55:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae5bc1ada2a0943690b92e5584fb18943eba96780782b4dce9be0346ded72b`  
		Last Modified: Thu, 22 Feb 2024 01:55:54 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7e6d2bf27219ff9747cd8d9417b3832d29e61d385b00e5f6bd562df63f202702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4615342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380dd59182350c07cda180a9a462e97b6cdbb97606d4561c31ef1117cc8420a`

```dockerfile
```

-	Layers:
	-	`sha256:c73e4cbab4e605094f59bd27447001a4c7000293081c1363d73ac76cfa8751ee`  
		Last Modified: Thu, 22 Feb 2024 01:55:54 GMT  
		Size: 4.6 MB (4584055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f17549e08a91eb4e356e5349f24cb650a4c613d8920ccfbafc8e757fe5c6be52`  
		Last Modified: Thu, 22 Feb 2024 01:55:53 GMT  
		Size: 31.3 KB (31287 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f119b22c9822cac4cce559746d3e989e15ee71b548f7aa58f5f1ef42f934c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130547460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d79bb2bb26db5c953e17b5454bf3f2dc2820cae5aebf505643737f0aeb5e827`
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
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
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
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f46bfdfc37d0885d87421a8a52e25e4341406e62d51f8b82e8c748c069f9fe2`  
		Last Modified: Wed, 06 Mar 2024 03:51:51 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baf76f4d6981c4ba88d28998ee3236e2977b79105aa0daf176b7a8db0e414ff`  
		Last Modified: Wed, 06 Mar 2024 03:51:52 GMT  
		Size: 6.1 MB (6079165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ea9dfe5c6876a6ba5f71d93d1f0d5163282774e6b2515adec8516486a93e8`  
		Last Modified: Wed, 06 Mar 2024 03:51:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f2375103336189961fb0577b4ad6d8df037889723bdd0931c0f6b2afefb2a7`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d500bb7f4311f66db96f7e93af9b0d49f84aca7b189e4ee6355a6c16613a2`  
		Last Modified: Wed, 06 Mar 2024 08:59:45 GMT  
		Size: 90.0 MB (89960505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9656e19536d5558f0e3af1278df43ed88a5f76acd35e5511c539a8d810b9bc8c`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b901ff85f7e41c532eaf210763d4f2ce29d7d3214adbf2d11ecda2fbf1ee5bd`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:165846614bf1140987aea837360d4519a3a1d28600e4bee0c647a896cf655911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15283c1d127aa03e48d6b2f6a60c7f024d04a5356633979b1e8545d93d058208`

```dockerfile
```

-	Layers:
	-	`sha256:496276516c4e207f8df459bb37b899d9b9e1902f3a785587a960d9c46374789e`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 4.6 MB (4585342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99667114042eab3560343960f7bfcdb22deef3fb0a98545be46995bf513058f`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 31.3 KB (31339 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:91ca0af67957264049fa4bf0e0b526908fe62a274c356ec4e036293d104aae70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121284380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b995060d749b6e7da50772019950968b3fe32376e21c4dfeec9f65adb2b66ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
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
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7def117eaee89dfe4e12bc6fa3a6f21300dcc92dacb26289bdf48ad2db1dfe`  
		Last Modified: Sat, 17 Feb 2024 06:38:37 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b65e7a2f88d5d85e9b21a7e359ebcce2cd4a2bf5b52877e3b6263350b23f12`  
		Last Modified: Sat, 17 Feb 2024 06:38:37 GMT  
		Size: 5.5 MB (5535295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb6c4e1166ce44d1dbf12aa02383b57571415756f9dfd9ae0a4074dea269aff`  
		Last Modified: Sat, 17 Feb 2024 06:38:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402f32a3b8b5767a2cf828a047fe8f6e1be564af1202b20bea3bccf8940f1af`  
		Last Modified: Sat, 17 Feb 2024 06:57:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483457d8a0b6e10696f99c179fd4d036097a93e5575ace60c8e56c33a18ebbb5`  
		Last Modified: Thu, 22 Feb 2024 02:51:46 GMT  
		Size: 87.7 MB (87726676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a5c2a5405cd7945d2ac7942e60558efe5ff5c5af475bd99e614f9ad433220`  
		Last Modified: Thu, 22 Feb 2024 02:51:44 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de231466317b15d04510ffcaf9ee5994d386bc1880c9d676b2cd515a67e4b1d`  
		Last Modified: Thu, 22 Feb 2024 02:51:44 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:0bb96769e3caa10471f4fa0557d99514b191a69c06cdcad629026cd7c72b9df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4585876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caee6e757e79263d86e4a438786bcf65879c76a5495757a6a04a48ca5bc904a6`

```dockerfile
```

-	Layers:
	-	`sha256:edf9ec70e908179d14ef75e829f49d56d83a74f5a2ac7ce71c4196831e5fa099`  
		Last Modified: Thu, 22 Feb 2024 02:51:44 GMT  
		Size: 4.6 MB (4554607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18428132b06f96fb620ccc7ab6b49316026cf816ba0b5c77e4b2e5f5dbffdf21`  
		Last Modified: Thu, 22 Feb 2024 02:51:44 GMT  
		Size: 31.3 KB (31269 bytes)  
		MIME: application/vnd.in-toto+json
