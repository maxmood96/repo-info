## `mariadb:lts`

```console
$ docker pull mariadb@sha256:590803c3826ecc14db1ac4a9cdb175d4aaf28c39f990eb1f9c077021fd0e9716
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
$ docker pull mariadb@sha256:eb9d7a8eeb0139cfd26a06ea248e6c8d1be82a4a85a22eb7d16c535d27687220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103841512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10247350efcbc2383c324c09d2d824aedb1e84d0a71c9b7bfcd5687c9f0ab91a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 29 May 2026 23:07:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 29 May 2026 23:07:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:07:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 29 May 2026 23:07:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:07:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:07:45 GMT
ENV LANG=C.UTF-8
# Fri, 29 May 2026 23:07:45 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:07:45 GMT
ARG MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:07:45 GMT
ENV MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:07:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
# Fri, 29 May 2026 23:07:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 29 May 2026 23:07:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 29 May 2026 23:07:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:07:58 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:07:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:07:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:07:58 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:07:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366cfd42e46267b7ff38c108d8f46925fa45591ee115d7243f98ec7ebe8e86a6`  
		Last Modified: Fri, 29 May 2026 23:08:13 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0c08073417e5143fdb568efd5af220b4a03c3bef8969bd457c9a87d44ae8d1`  
		Last Modified: Fri, 29 May 2026 23:08:21 GMT  
		Size: 5.3 MB (5288136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aca2e94abb17b857ed3e500d8fed7c96f715087134764b9573843d5501864f1`  
		Last Modified: Fri, 29 May 2026 23:08:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0eb5a3ff44d941545670ae454ab624dd5f8bd55639ea88841ea1e6af08ea4`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d155db2492ecf07d170ac121b8f5efe8f3d14adc7ef703a91a49f7641d9b9578`  
		Last Modified: Fri, 29 May 2026 23:08:39 GMT  
		Size: 68.8 MB (68806078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3daa49cefd16020559e831a96be051453f995dfbd7fb20eb36cf52c6db8f8f4`  
		Last Modified: Fri, 29 May 2026 23:08:19 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd588650ddb2b48b8067406b5e62d04ef033a0029cd9f68da291649e0de981bf`  
		Last Modified: Fri, 29 May 2026 23:08:21 GMT  
		Size: 8.5 KB (8496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:2929f0ae9acb007f06bf196fbf15941a95dac09b7f59f9e207c556d032253b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a7a3aeff64913f3d00a53a4329d3f3ebf37daa69dd30a2f994fa8a65ecc090`

```dockerfile
```

-	Layers:
	-	`sha256:9bb38742a09ed066c4d7044dd8c5ac26afc66614e6ef5bd6c7c39e5c5c0cb42e`  
		Last Modified: Fri, 29 May 2026 23:08:21 GMT  
		Size: 4.3 MB (4274514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f4b329c977e93c27425815a40c3de7e89706b6fe837a60448b289589e145ed`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1316977359b94c45d320ed4b3244a0b37940850e0fd1e22e59bf9e50e0679aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101976010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57bad2c64734854e9ac5d9d0e2fadab8f0333c09b519c35139283755ee24b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 29 May 2026 23:07:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 29 May 2026 23:07:53 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:07:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 29 May 2026 23:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:07:53 GMT
ENV LANG=C.UTF-8
# Fri, 29 May 2026 23:07:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:07:53 GMT
ARG MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:07:53 GMT
ENV MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:07:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
# Fri, 29 May 2026 23:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 29 May 2026 23:08:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 29 May 2026 23:08:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:08:08 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:08:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:08:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:08:08 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:08:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575115b7c8f76099236a787f6fd0bad27806198c9aee435b165afdb3288ef37e`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126977556dcb4c58af698ba39a3ed7dc2770f1cbd3cac7027ac0346cf3db8749`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 5.1 MB (5098533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d6b63b59a88754bcb28b6a04d91afdf869faa5818fb9854e8e670bf87c83f8`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa841d68b9102f4c0937c90d1db6617eb16de0e4f8e391be45206fe91afa91b`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d082508b4a30afaeb468dcba8d307be4dfa61937156d7e481bba97ee61590434`  
		Last Modified: Fri, 29 May 2026 23:08:26 GMT  
		Size: 68.0 MB (67987370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f34c70eb818e595a3b19e9af0e57aee6e48a0b0ee38e9c7f2dd21ff5f7398a`  
		Last Modified: Fri, 29 May 2026 23:08:24 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01e8bff4f44c18d2186b8c25218604c8dd776959b9b3a6413fb2606dc71a994`  
		Last Modified: Fri, 29 May 2026 23:08:24 GMT  
		Size: 8.5 KB (8495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:cd7d38d0521b6cdd61b29b0a268daf231622e13761f0809075733f17a20c2453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cf9d0a6048344092df216b30d49ce5a2cecd8cffe20d80c150075714046d38`

```dockerfile
```

-	Layers:
	-	`sha256:246033b7239c4655f76ab4b57355c9ec766aef547ba78f2035deb13d0a659dc4`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 4.3 MB (4281791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460ed32a9858b7b4cc73f0c8c0299a183de520f911a28adb50d14cc07c96eaff`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:82aefbf794b0870c2753e1c36e6b66fc358e508385a44b2e1126eb0d127449a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113764561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cc7ef993278e7b7fd126ada2ad4ea4a929f48ebc3ea3bd352fb0d4565e47d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:32:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 20 May 2026 18:34:14 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:34:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:34:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:34:15 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:34:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:34:15 GMT
ARG MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:34:15 GMT
ENV MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:34:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
# Wed, 20 May 2026 18:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:35:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:35:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:35:00 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:35:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:35:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:00 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:35:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ab6ca40b38a1b6ad029a23b02c6f38d37acddd780bccad2fe6a872da77e42c`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4183776bb3052cb352302661ff638d9d3fa37fbb73f2d193344662bca766db0`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 5.9 MB (5927651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cf481b7143192448683cac79bacf443d90e1285b373d223a51197aaac8272a`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4337ed89914f2d6afbc89d4e23b1bb220bbf5981a184ef3877fa61ad38299b0d`  
		Last Modified: Wed, 20 May 2026 18:35:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceed2ed11499603d62c07f84281e53a28fd2e85e05e658111ddecaddc36af14`  
		Last Modified: Wed, 20 May 2026 18:35:37 GMT  
		Size: 73.5 MB (73508489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caa8e08dfbe4c08bb7e15795c4bb98aa124d7c3e147baa25737dfdacbe3c282`  
		Last Modified: Wed, 20 May 2026 18:35:32 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59b5903c7d06bcfd7cdaed9b76a4feb00639ef2aff4af3777ceae607dba7e6`  
		Last Modified: Wed, 20 May 2026 18:35:33 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:728d5db2d30132d9e60753ef677ab22b6eb0069c0f21f3cf26a5357168785205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a7f3f1239102a1b6e6b0d45a06e6f8985012271de87d4ce8c0e17683741eb1`

```dockerfile
```

-	Layers:
	-	`sha256:5eca64affe4f663895213884baca44a641e26b8b2c2239fd78592b353db998ec`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 4.3 MB (4282449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea56727c7410cd43fee53e37f875fbf4217d4c97ee86d7c99393c549c0606f2a`  
		Last Modified: Wed, 20 May 2026 18:35:30 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:5cf8a21921d65dc4c627b4fac1f1d64669321fc6fc8a06e13cd212ed71c8e40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108150945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aa912b87a4362de2fdbb48fc34fad00c4fdebbc54bc49dae64f981951286b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Fri, 29 May 2026 23:11:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 29 May 2026 23:11:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:11:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 29 May 2026 23:11:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:11:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:11:36 GMT
ENV LANG=C.UTF-8
# Fri, 29 May 2026 23:11:36 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:11:36 GMT
ARG MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:11:36 GMT
ENV MARIADB_VERSION=1:11.8.8+maria~ubu2404
# Fri, 29 May 2026 23:11:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
# Fri, 29 May 2026 23:12:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 29 May 2026 23:12:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.8+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.8/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 29 May 2026 23:12:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:12:45 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:12:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c5fc62f9e2a69f996833d126b7e99fb1871cc246597c9606e19dcfe5a8e1b`  
		Last Modified: Fri, 29 May 2026 23:12:11 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a94a5e57ef5b275c85fe4055fb84a8f1c8d2aa2c037b20ee38760b251e8e42`  
		Last Modified: Fri, 29 May 2026 23:12:11 GMT  
		Size: 5.4 MB (5443857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736645f3c2cee87f3a2acdec4e5435f89f088153c773963d80ce3bf287a062a`  
		Last Modified: Fri, 29 May 2026 23:12:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b927e0bd88e2377a16b8a0f9aa3e122fe3f9765a2cfa6f70160e1fa4165b1526`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e559fade07ec7ef5aa3d29e44aa0743172555ff53708047b9e2885b33cd7924`  
		Last Modified: Fri, 29 May 2026 23:13:13 GMT  
		Size: 72.8 MB (72780624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b4c8a0280e13f2cf4dc2e209001854f40b3f34358a68afcea50e89238b1f38`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 4.0 KB (4031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c52d3f62c378f64347acb517127b6fff9680e66db3a0a8b97b8d1fc352d78`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 8.5 KB (8493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:f3dbd6a35a26412bde8d5d98cec4996dc1ddb41e5d112aea7786607e6d3b1031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a36290118c6fca2b91360038f22a1211f3a08553254b114f19831ec84819481`

```dockerfile
```

-	Layers:
	-	`sha256:ec02cfe428b15350f03a1d8cb713a4885cad875a5b24fc192bc89bb8f97df696`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 4.3 MB (4276233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd505d892f3244a24bfd6231bfba41008d6e8d55cc0807c7ac85bc1cbb4756cc`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
