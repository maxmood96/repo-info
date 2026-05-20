## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:8acd4a5561e8897cfc8a99480f25bcecb10b726fa17b1ec7381c6ef36fa00a79
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
$ docker pull mariadb@sha256:36d97729dcf3ccbd4b62252b7592d9ceec6bb392b5a10126681aada4d9fb7bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104084159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4e99c5004ef3759ee7d0d9eb778cd82a004b5f9b61353440bd80c5531ed6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:35:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 20 May 2026 18:35:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:35:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:35:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:35:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:35:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:35:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.17 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:35:53 GMT
ARG MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Wed, 20 May 2026 18:35:53 GMT
ENV MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Wed, 20 May 2026 18:35:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
# Wed, 20 May 2026 18:35:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:36:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:36:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:36:07 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:36:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:07 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:36:07 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969ede67bf4fa643bc910e2f4e78454eb32927710ac68bfd8a93aaa7fbd0eb4`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1dacfe225d6ce2eed0f33e062cbc220c477536baab35ad3bf56eaeb2fc3b44`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 5.6 MB (5613921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea65ec9b96ba619838d6563f0c8f40498dfaf4a1ebe6fda40bd5f80d15b1fe`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a1391cc290586f7ac9ea432be84bfa9fabcb14530babce2bfc398d78086d7c`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368110c5c46eb7938a0c25c6be697bf629e2f7ddce9d011c8f8fc565ec721f9c`  
		Last Modified: Wed, 20 May 2026 18:36:25 GMT  
		Size: 68.7 MB (68718978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3865f3980ff111e850633c6153f265cd7bd1fa6ce5126154423f9f75243c4a3`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5a31247ac20b8490efbf27e28fea850a9f42cae8080d2d4df033eaf3917e55`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 8.4 KB (8381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:de97911c9a2c5bec2139b2389e9cae69a9c02e8fbd701226a3e6a8981040e979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4832342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c06ba7903b2dde6a54c0713d1d482a504e5ce8f645e1755684dbf44f7142aeb`

```dockerfile
```

-	Layers:
	-	`sha256:0b3f63c8297f6ad7e0ac025ce57526b5f6c5ec906bdfd90aff7a457c40a849d1`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 4.8 MB (4801435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fb52d1b8ea42bcc85ec4f3cf7fafd627d95cb1a230b31fa6dbb7b563896c9b`  
		Last Modified: Wed, 20 May 2026 18:36:22 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:bb9f10d2065d572fe201506a6c682178065574b20648bd3bc9f25aaabe840969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98628148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248927a5b11a09dcd0c3ff02d600e34c0315b5b3b7ec9c24db8460f92f8175db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:35:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 20 May 2026 18:35:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:35:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:35:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:35:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:35:19 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:35:19 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.17 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:35:19 GMT
ARG MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Wed, 20 May 2026 18:35:19 GMT
ENV MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Wed, 20 May 2026 18:35:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
# Wed, 20 May 2026 18:35:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:35:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:35:35 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:35:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:35 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:35:35 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c035f0cae45c07468be9c2be224de3a11c4a1e916f4fb7a8d63dd9973f6465`  
		Last Modified: Wed, 20 May 2026 18:35:51 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c644798a62679352f2a20809e7b1ead2e8f1d55ab761011ced3631d74e5e0af`  
		Last Modified: Wed, 20 May 2026 18:35:51 GMT  
		Size: 5.4 MB (5448838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f9727fa2bc1f8fd93cd01f66b6a69c7f91fd10e3e4663cd8f5782f8e5719c`  
		Last Modified: Wed, 20 May 2026 18:35:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d066ea15a247d9bfe911cab227577676dc294476d7cb31657e0351c49f7284`  
		Last Modified: Wed, 20 May 2026 18:35:51 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861a079e62337efde414676ee3170ea861b0279db455b8fd5c59d5dc18f1cd9b`  
		Last Modified: Wed, 20 May 2026 18:35:54 GMT  
		Size: 65.6 MB (65558109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05adb3adc1e3e19a1640a72485fff8c0bf3d09893957d4e1055bc575e84eb0`  
		Last Modified: Wed, 20 May 2026 18:35:53 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c63badccc193885d907c1647a3ad993f4975dc1ef06b0b033102919f3659fb`  
		Last Modified: Wed, 20 May 2026 18:35:52 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3fc4c9a2708bac7532a445982e7740c235fdb9681ee403e0853a268d60fed3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa852fedd60220494f60be9d3c699c6dea2e464cd2e7935b7c520e4e4efbc205`

```dockerfile
```

-	Layers:
	-	`sha256:e9588694b65af7b63fa810be3946fb485ebe46f6f2554f6253919940a289b06d`  
		Last Modified: Wed, 20 May 2026 18:35:51 GMT  
		Size: 4.8 MB (4807873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605b488d653d6cdcb336c98d1217846374995761579460b5ffa94da1fce4b842`  
		Last Modified: Wed, 20 May 2026 18:35:50 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ba16b95354ab5ba56485e8703689b67bfd5dbefd3da6d2864bcd930ea61ea210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111655535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02564c1034033714fdc2ac058eabc967208d2e68f69e2627ed208bbed3dd4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:30:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 15 May 2026 21:30:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 15 May 2026 21:30:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 15 May 2026 21:30:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 May 2026 21:30:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:30:45 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:30:45 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.17 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:30:45 GMT
ARG MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Fri, 15 May 2026 21:30:45 GMT
ENV MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Fri, 15 May 2026 21:30:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
# Wed, 20 May 2026 18:41:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:42:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:42:17 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:42:17 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:42:17 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7559727b359c9fab6a08b01e489736028d58cef743fc06c4c758f3d1e38339c`  
		Last Modified: Fri, 15 May 2026 21:32:02 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5de40de847f44679b97d3e63e64bb99110e7cc7864592e5080a7a00d61337a`  
		Last Modified: Fri, 15 May 2026 21:32:03 GMT  
		Size: 6.1 MB (6106885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13961c06cf87db010c266ffac814cbb016c11c1e99a567bacaba54f42de3e3d`  
		Last Modified: Fri, 15 May 2026 21:32:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a33bbbd00cf1915b4970a1d5c3a79f8fbe16943f2ee604eaadbdb7ae95fdd`  
		Last Modified: Wed, 20 May 2026 18:42:51 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b1043161912ed4c9359d6ab7d686d7f27be3a61cc6a17180f771cb558fdd7`  
		Last Modified: Wed, 20 May 2026 18:42:53 GMT  
		Size: 70.9 MB (70887355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cf416d0d08cb72561f569a13b963c4abddb51ed93197363f1948c9f9e170aa`  
		Last Modified: Wed, 20 May 2026 18:42:51 GMT  
		Size: 4.0 KB (4016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa87fe06b7c95f1c7acccc0caa9a284d1774cedc58e4753e3daa2774a6f2af2a`  
		Last Modified: Wed, 20 May 2026 18:42:51 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7fa3b531123c10aab1cd11c8814ebe22554802e726208d0a7119d8fcad1a7db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7edc8a9d0a3c5a8c7259321c2052f82cc5d4c2c73c9c8cce9c795965b947a53`

```dockerfile
```

-	Layers:
	-	`sha256:bf36921a996d98e5840371ddbb71c5f6a0d636d71dd21b318b3fa4f71a1d0b69`  
		Last Modified: Wed, 20 May 2026 18:42:51 GMT  
		Size: 4.8 MB (4809243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9249a3c85977bfde6047765e7e54496757b77235b0d57b02b7b56fd6e8e712`  
		Last Modified: Wed, 20 May 2026 18:42:51 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:2b59793c2b3f78fab824933475bd2f09937e47cd41e52acb331c241ef720303f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101701466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d202473e57724199e067843a4ad34b1e69991fff69d5472a6f0b9e77e0261040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:27:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 15 May 2026 21:27:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 15 May 2026 21:27:47 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 15 May 2026 21:27:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 May 2026 21:27:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:27:48 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.17 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:27:48 GMT
ARG MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Fri, 15 May 2026 21:27:48 GMT
ENV MARIADB_VERSION=1:10.11.17+maria~ubu2204
# Fri, 15 May 2026 21:27:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
# Wed, 20 May 2026 18:55:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.17+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.17/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:58:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:58:26 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:58:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:58:29 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:58:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6c9feba10433e497572e6a29d7d9ae5db0910ab9cd5c5d3e4fedc20d7a852b`  
		Last Modified: Fri, 15 May 2026 21:28:57 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec32e76ad3246f8f15d0724af5654adb65c0f9659a9f84df3afadf19eff69969`  
		Last Modified: Fri, 15 May 2026 21:28:58 GMT  
		Size: 5.5 MB (5501919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095cb9fd2d58af8ffc589fd83193be135a7b6d3075fb6e23320b5a61c47d7606`  
		Last Modified: Fri, 15 May 2026 21:28:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8aeb3c79eacefce6342210e7496a65e7d0911fd1c40e4f4ab70ddc09aa06c`  
		Last Modified: Wed, 20 May 2026 19:00:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69478c065d99fbd0b3e0f6cf3ac4c5b3a919abc6ce76b4adc7b90fcbeac8cc3c`  
		Last Modified: Wed, 20 May 2026 19:01:10 GMT  
		Size: 68.0 MB (67982670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a30fcd9eac5de268c5c53b51127aac231a03ce0d1d69ea59748398194cecee`  
		Last Modified: Wed, 20 May 2026 19:00:58 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9990380de21ff11e606e2d62b77ae8b8e5f9a70a994f3bb176c84ac4ebd981e0`  
		Last Modified: Wed, 20 May 2026 19:01:00 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:d21e385180e28f38813be84d4c459d75a141be00fd582637dc46d89c5161481b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4832664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0536652429c94219e98919ccc02cc7c86c409cca676e1d620af8b6e43162acc3`

```dockerfile
```

-	Layers:
	-	`sha256:9ab3713916972027212dd05b08947921125080234beb29f1855db0682d15c04b`  
		Last Modified: Wed, 20 May 2026 19:01:05 GMT  
		Size: 4.8 MB (4801758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e9b79dad7c0eb59a7f4ad034ba5592934f69c36e1c393761c1489f5a394bab`  
		Last Modified: Wed, 20 May 2026 19:00:57 GMT  
		Size: 30.9 KB (30906 bytes)  
		MIME: application/vnd.in-toto+json
