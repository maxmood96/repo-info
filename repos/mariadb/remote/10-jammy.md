## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:e2772bc4ef602b41ea44192be6a6ea46b56f4dbe6d2fe70e2d33ff8a01b4915b
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
$ docker pull mariadb@sha256:0a2c136bd7f771adcefe93b8cc828dcb9a451d93b305492fcc463f882f96b97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122395734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2af619908a56210a704427edea5839fba25c251122ca86271237062d897c1f`
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
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
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
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e214e6737d8fb8119eb73eae3a8a55490b4c07e064ec530b1bed3fe736594f6f`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f0c6ea1b52a52ab6e042dd36ea7bf8a0c1826037654587893a868a854777`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 5.6 MB (5649827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b26a2f888b920916b631650e255030a0494c2e3c6ef060632fa240f6030cadc`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edc50b97c9b432709bd588e9f59fedaf1a60d45eec041a0192beb9deec14f15`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c975760206132ac66e98815e4323904597653188888a5e4a3da026030f6097`  
		Last Modified: Fri, 02 Feb 2024 00:55:44 GMT  
		Size: 87.2 MB (87183335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c8eda6426e8ce56810e1d485c1da7991bd7ec6c900c18cbf0c19515afe13b`  
		Last Modified: Fri, 02 Feb 2024 00:55:42 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5ed3fd578b20ea5386d4be91e760920cf9991ae5efc053fae8cf9d063f58a5`  
		Last Modified: Fri, 02 Feb 2024 00:55:43 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9b17ce98f87e2c9c5f52e6177212d72cecdaefeb32a42e13d5b528de20b4d2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0404cfd9352cc0e9af40f9f69e7985146377bed4e5a77b5021da95690c9245`

```dockerfile
```

-	Layers:
	-	`sha256:56011a0ab0ed0d64db1bcdd3b9d4712da39e07b84d7a479a6d61660fe513b567`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 4.0 MB (3978012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aa8c9707979b58d1f13363b1741a6942a77801965ae30484e07487e2705c1b`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c35cdac4d0b9bac0b7f20126ef79ec087f5b16fbea5dce2604475f70f105cb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116768570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1993bbfabb1a1c34e8b4dfd5308886d0539d30c76cf1f938fd4ce2416a1ff7fe`
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
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
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
	-	`sha256:ce9ebea987c26664d067f7e14c93231c6d303e4acb322f15ddbf05b414646d64`  
		Last Modified: Thu, 11 Jan 2024 17:49:04 GMT  
		Size: 27.4 MB (27356849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43435310a133deec429f730e39b8c1fef582ec530d64f96bbe0574a56b0bb702`  
		Last Modified: Thu, 18 Jan 2024 17:27:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef59ed3a45af9068dbb1c7b42eba2073a69bf26c564dc2435a7663443d1dd8e9`  
		Last Modified: Thu, 18 Jan 2024 17:27:31 GMT  
		Size: 5.5 MB (5463373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aab0cd9669420781245cbdc5e5ec0fc99950fa14d40aee49ee9a54a4fb5d890`  
		Last Modified: Thu, 18 Jan 2024 17:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157a6d12b9f369235d54cafc9b6a49901b155d3867005700876757c1d0205fa`  
		Last Modified: Thu, 18 Jan 2024 17:28:53 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48197f23a9458a0cf55e637847e57ed1b8c22ddba593a5d8264f509818fae58b`  
		Last Modified: Thu, 18 Jan 2024 17:28:56 GMT  
		Size: 83.9 MB (83934700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec8c498c8553b77ab7331c81f170bff71e45fb003881c0313409aa731b3667c`  
		Last Modified: Thu, 18 Jan 2024 17:28:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9165aa99b5699c9b53aaf8755918b31ac7259fb069354d72f318c599dbd2e`  
		Last Modified: Thu, 18 Jan 2024 17:28:53 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:6fdb14e2335b0b34ff4697d561d1d852dfe2c56a85cc0b7c937f9ade61becdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddfadbffc419d3158104fd653388895048089a18418ad38113e4b1d66ae1a13`

```dockerfile
```

-	Layers:
	-	`sha256:1a652fd864e73b8b09c2269fb8ac6378d5a3e8d286ede69e3f57a2c9ab54812e`  
		Last Modified: Thu, 18 Jan 2024 17:28:53 GMT  
		Size: 4.0 MB (3983760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3404ec6a998636eae74a7ffa778c2a24589f3ff5a2af7b6cd07484f7632d79e0`  
		Last Modified: Thu, 18 Jan 2024 17:28:53 GMT  
		Size: 31.0 KB (30992 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:35fa155766b7430dac13f3b5ebbb3a2179f52aef9f4808d09d92baf71d94329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130491637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b6315ad32d9df79b0502e92e7a9a0f42e926d1b08676da389709fede38ad58`
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
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
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
	-	`sha256:eb06c458f1bcffd534bd10415f36af10d84ad0223c7840a052931ee0238f62ee`  
		Last Modified: Thu, 11 Jan 2024 17:49:17 GMT  
		Size: 34.5 MB (34519608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bfdf8789332dce06539e3c09d832818de741f1416ec9b0ee53c4d813c167d2`  
		Last Modified: Wed, 17 Jan 2024 04:09:54 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd5103548409201bc89f22e40f9f805c84d6f64448e65c9e44124d74124f5d5`  
		Last Modified: Wed, 17 Jan 2024 04:09:55 GMT  
		Size: 6.1 MB (6082046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5be8e8412bf8f27e37aaff3f316a1cd2e751299859f08488ab018cc63db6ca`  
		Last Modified: Wed, 17 Jan 2024 04:09:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c16ddd608199a5ed8207fd0541aa07325c1e42da17c7b2c3ac3fb2ac6575046`  
		Last Modified: Wed, 17 Jan 2024 13:08:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e0baf06e76d3c5673a66b0741b7ac46d6cae28a34ec7f19d2cb45b24a6089`  
		Last Modified: Wed, 17 Jan 2024 13:08:24 GMT  
		Size: 89.9 MB (89876341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552eae3664888e5f9400f0c3535144018e15a13e59dd6b6c93d9d0c867f182a`  
		Last Modified: Wed, 17 Jan 2024 13:08:20 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5cc9ab932bdfde0f7f46f85f0353c1584a193ed8e4c327edb5b264fe92107b`  
		Last Modified: Wed, 17 Jan 2024 13:08:20 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3005877b90cb343515a603b26a956d94bfd7ad10964075ed2c46c4db3455d473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f950711538ff5eedfc5cfd2366be678b5f1e9b242adcf27652c816069d735b`

```dockerfile
```

-	Layers:
	-	`sha256:784fce75b2ce4372a4b8acadf094157fb0e998c0835fd010848f86f0a4fc2adb`  
		Last Modified: Wed, 17 Jan 2024 13:08:21 GMT  
		Size: 4.0 MB (3985683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e85ad989c464e86a4ac690c6dd5846393501ea1f37b3f153fb30acb3711531`  
		Last Modified: Wed, 17 Jan 2024 13:08:20 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:e679384a77214f5834f7d7ead83e6c5a963233db8c9fae8d29df1348e92dd13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121203952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df06feff9e79bbd56d8000abf5deb2d6633055946da7d71071471786596eef`
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
ADD file:5ae109128826d2e7660949ed9ff9af4b92bbade5ce06a7011ab7b15bb21d8b75 in / 
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
	-	`sha256:c0aadca0a59447759d5cf02c0250d916b74c90d22c4451a011b645d79453f4fa`  
		Last Modified: Thu, 11 Jan 2024 17:49:24 GMT  
		Size: 28.0 MB (28026713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31012a710ebef17cbda8b429f167f19dfa7ffcd35319fcc5dc12887d850368b`  
		Last Modified: Thu, 18 Jan 2024 15:35:24 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ec398eb3e28465acd899d5d163b3bc723e45eeebf0f7b7b889a1bfe320458c`  
		Last Modified: Thu, 18 Jan 2024 15:35:24 GMT  
		Size: 5.5 MB (5535282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955c336fccabb852893c18269ac2fe5f7fa7befef85d6e32398b38b948328e7`  
		Last Modified: Thu, 18 Jan 2024 15:35:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4989ef1cbbdfc75b4d70204e0f346f5922e92515b18d81684e33c8ee34640e96`  
		Last Modified: Thu, 18 Jan 2024 18:30:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1277184d1d244cdf8ea290d1ecd0626aeb8294a31625027ae9670b7af7240d`  
		Last Modified: Thu, 18 Jan 2024 18:30:14 GMT  
		Size: 87.6 MB (87628309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae96228607bea9a46329fea3d394e9acc0c8cd02477f1b1b1e1fbf6dcfe158c`  
		Last Modified: Thu, 18 Jan 2024 18:30:13 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae2c9e46c8372b0905ed28ca048428c95ddee778d82bd339ac22046a8789f4f`  
		Last Modified: Thu, 18 Jan 2024 18:30:12 GMT  
		Size: 7.9 KB (7861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:c1dd759db3db9a9d3ecc9248234a838e224665807ea7793a6a70b46733e69824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca98887968a4d850827269dcb55c4be895ad10692d9c5fa419e0b42fe57ba5b`

```dockerfile
```

-	Layers:
	-	`sha256:86aea7026189ebdebdd07e28ccaa9855223ab7498def615cf259cffcc7a37ab2`  
		Last Modified: Thu, 18 Jan 2024 18:30:12 GMT  
		Size: 4.0 MB (3956008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d3711879b5665e46de925501a5d27e28f8fd92a9ba502aea06fc9ecc385163`  
		Last Modified: Thu, 18 Jan 2024 18:30:12 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
