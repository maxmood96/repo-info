## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:8a99982dced50264560fd8ada91aa34c276636bc02713f01f252c540930f9915
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
$ docker pull mariadb@sha256:9fb5c752a7c6e10b143ec6637a666e68b37453cbf8b726e9eb1c96c5b7d66b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106495610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09758891b16de42b092ca908a62794165758b2563915bc41d570cc648e10d83`
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
# Fri, 15 May 2026 21:19:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 15 May 2026 21:19:59 GMT
ENV GOSU_VERSION=1.19
# Fri, 15 May 2026 21:19:59 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 15 May 2026 21:19:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 May 2026 21:19:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:19:59 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:19:59 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:19:59 GMT
ARG MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:19:59 GMT
ENV MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:19:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
# Fri, 15 May 2026 21:19:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 15 May 2026 21:20:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 15 May 2026 21:20:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2026 21:20:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 15 May 2026 21:20:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 21:20:11 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 15 May 2026 21:20:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2800455c4d272983307def273de63d247a93ea077757328ba8e3d87e563ca79`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ca2650004cc64c132bc30472f80c1be872d56c5ce9855ed160ef89b377d34`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 5.6 MB (5613926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024d7c7813fb6e15d8a1e174cb3fe94dbd89daa8b8d426169e5acafcd003bfca`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a923cfa0de1b6ab2f8983b2d73d8bac1b73077cbf35cd9690de8fa06d85544`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b44f7496056a6fd561fc84e04a11600f37cc96b458907fb41270deecba26c2`  
		Last Modified: Fri, 15 May 2026 21:20:30 GMT  
		Size: 71.1 MB (71130444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3371f993deadcf520d66b1c8e566dea29fb13ce6a782ef463c98d9d5b9846a`  
		Last Modified: Fri, 15 May 2026 21:20:28 GMT  
		Size: 4.0 KB (4016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d302964c2fcaa393c4097a1b45d4fa1a2d6afe6ce9bc5f764df58bfbee40bbe9`  
		Last Modified: Fri, 15 May 2026 21:20:28 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:95d439d1ff28bcaa933f12c990bcae0208fcc10d257b141271cd63b2ed1d97b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4832342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97badcdedb38f4a04431c18868b2ec0d7fcb1c0ae62d14608842591b361d587e`

```dockerfile
```

-	Layers:
	-	`sha256:1c9a92db7bfd0c130d66dbca6db8e407cc4ff0f0def7d78ada5bea44c6ff737c`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 4.8 MB (4801435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c11413f9dd98a2106b6fb71be1aa53d936984645df0ed283084638e3607de9`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b77b372c1a0735fa4e60dbe64b27ec3782103953f436f643f090e8fc63b9ff63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100958906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb709489210f4d1ffc0ea490c356f3727b6edc369bcf5cfebaed3ce330e5546`
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
# Fri, 15 May 2026 21:19:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 15 May 2026 21:19:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 15 May 2026 21:19:54 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 15 May 2026 21:19:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 May 2026 21:19:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:19:54 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:19:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:19:54 GMT
ARG MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:19:54 GMT
ENV MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:19:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
# Fri, 15 May 2026 21:19:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 15 May 2026 21:20:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 15 May 2026 21:20:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2026 21:20:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 15 May 2026 21:20:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 21:20:11 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 15 May 2026 21:20:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d56436cc745a3367f03360137b13733d599d9ceb6408d214fc7bb277ba5cef`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a4fa3a2b0a6136eb8547169e5ef6100650f8070a5e934aeac83c682bfe77ba`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 5.4 MB (5448829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa09c12d997e7f521e420fb9e086a40eb654b98d5f8a32c351fe3678240c1b`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e37a6f5d3d6d9534b41701c16e99c3953cddc6d022998ca03d52cc4e36698f`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3c6713c064b9167154955559ade5b96b7b8a1c863abf43d0408a882c07c811`  
		Last Modified: Fri, 15 May 2026 21:20:29 GMT  
		Size: 67.9 MB (67888891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45d5f0f6f7ff0de8b9f0057019204dd526afdfd2c8e7d35eaab890b7db7005a`  
		Last Modified: Fri, 15 May 2026 21:20:27 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bed62a42483a363a6b2a000155b336b7412a6d70800c24ca9038f37e3942a5`  
		Last Modified: Fri, 15 May 2026 21:20:28 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:ce356bb75d319a3dcba94dc4c34c48fd1901c37479ed60e7a04d93343d97c1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ad8c1a4db1e83d81f3f42ce6b21fc60e0ff1b0aef34b730510cc3dbd1f5558`

```dockerfile
```

-	Layers:
	-	`sha256:f637198203c6555bf7a809825b3aea847be2adad515399be5e1aec838737c1b4`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 4.8 MB (4807873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad817f8aa081b21ef6a96da3b3419592327cfc555492a4fff6405d3ec00aa980`  
		Last Modified: Fri, 15 May 2026 21:20:26 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dec154ee8b3a2df31c3f10d63aadda5e462cdb28ec84d6c3fa8716da57d3dc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114202714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd550711ff7a9d22aa92d594c654aebb15de871355e4d7b2963a1c171731df1`
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:30:45 GMT
ARG MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:30:45 GMT
ENV MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:30:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
# Fri, 15 May 2026 21:30:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 15 May 2026 21:31:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 15 May 2026 21:31:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2026 21:31:30 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 15 May 2026 21:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 21:31:31 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 15 May 2026 21:31:31 GMT
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
	-	`sha256:11a8972360a1faf855d78c27abfaeb73cc8db51227d1daf68b11b719b4db9269`  
		Last Modified: Fri, 15 May 2026 21:32:02 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a85a85466a4fc8c83a9df7220fb9966e6c1c822fe6b4906e334bcc10ceaf57`  
		Last Modified: Fri, 15 May 2026 21:32:06 GMT  
		Size: 73.4 MB (73434553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387a989a3b8f68ec7149235c92388df58c69693fc652c55ddff09035e49d2059`  
		Last Modified: Fri, 15 May 2026 21:32:03 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce14666d726b02241f7a1e3e0de123f9fa537c261949caf053f844ca8cf522`  
		Last Modified: Fri, 15 May 2026 21:32:04 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:66d0e787262796dd513117acefab6b2e1ca520d762b69534c96e5489e1ba341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d127befcdad0244a96bb92031a5dc7d71d2d2352107ade2705566da9b5863f`

```dockerfile
```

-	Layers:
	-	`sha256:78e4b90079e1b9ebf7e3b5be29da335b93035ddb1d85c4404e210587a9f3fb56`  
		Last Modified: Fri, 15 May 2026 21:32:02 GMT  
		Size: 4.8 MB (4809243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462ff90305e06c65bfb3f4f52ff362e4315e26e25fc8f6d71f3ecb20e390bad8`  
		Last Modified: Fri, 15 May 2026 21:32:02 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:53f4728bb4347ca401dcb91d20a96f0b94869a6baccc2b3c9e5bf4948e3b698e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bec0c7274c5d24e5cfa62d2d68720340e724fca0bb21d960c855fcaaf73794`
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
# Fri, 15 May 2026 21:27:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 15 May 2026 21:27:34 GMT
ENV GOSU_VERSION=1.19
# Fri, 15 May 2026 21:27:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 15 May 2026 21:27:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 May 2026 21:27:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:27:34 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:27:34 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 15 May 2026 21:27:34 GMT
ARG MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:27:34 GMT
ENV MARIADB_VERSION=1:10.11.16+maria~ubu2204
# Fri, 15 May 2026 21:27:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
# Fri, 15 May 2026 21:27:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 15 May 2026 21:28:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.16+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.16/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 15 May 2026 21:28:21 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2026 21:28:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 15 May 2026 21:28:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:28:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 21:28:21 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 15 May 2026 21:28:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ccdc300e321e0cd6df9bc9c632e27fe62de6acbc56fc77d06792f436a54018`  
		Last Modified: Fri, 15 May 2026 21:28:58 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e06456cf4494342dee837b6d31a4e5dd1c22e599921a2e3ff89d6147af65b33`  
		Last Modified: Fri, 15 May 2026 21:28:59 GMT  
		Size: 5.5 MB (5501845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2dcec48bca784850752ac1447c8702ef8d60c73eb6e3dd5aa7c751e972e36`  
		Last Modified: Fri, 15 May 2026 21:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318bb9fcd1c6f0cafe2b3e73983153edd4485c1a5b95aaa3ddd12556d4f9abd`  
		Last Modified: Fri, 15 May 2026 21:28:58 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b9d440cf1299c25e82b7539fb972eccef16ccc6915cca5e24d8803fe50867`  
		Last Modified: Fri, 15 May 2026 21:29:02 GMT  
		Size: 70.6 MB (70613339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce3d163579312f35e77207dde3e210b98cc8b451fda5a3e7aa29e54c4ff2aab`  
		Last Modified: Fri, 15 May 2026 21:29:00 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11334b96daeef39a30b59d3c6df82f4ae982e3c71d67f35ecbc1dc381654824e`  
		Last Modified: Fri, 15 May 2026 21:29:00 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:17d02fcdd1a16793b09d69d57cdc610e447b576b6acdb0b1f5a46c650e7771e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4832665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ef7a8efc5f6354975b5f0f340b0bdd98cac8bcdf81c6a6aca3c54d0c39db0`

```dockerfile
```

-	Layers:
	-	`sha256:cfd2c80981d244e92d0d1bbdbac9512fc9b82dd55e72b2f7c88b981834806fb0`  
		Last Modified: Fri, 15 May 2026 21:28:59 GMT  
		Size: 4.8 MB (4801758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc714a3d9a59c3de5b6e044e631e0918385adc1f3c9e6bb2da480aa952d6ae1a`  
		Last Modified: Fri, 15 May 2026 21:28:59 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json
