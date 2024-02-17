## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:6352a28969e9c6309ccc9d6aa7ec05e00303b9cefb0b61d7ccf11947d30500ac
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
$ docker pull mariadb@sha256:3e8785c608dbc3c17c59b7fe6741cbe833ac022cad30e48928f2b84f88459121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122467607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63ac3bcce8f2a5ae6bbcda1953bb2e621c0447560fe8590fb8b867224bd323d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 11 Feb 2024 23:03:42 GMT
ARG RELEASE
# Sun, 11 Feb 2024 23:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 11 Feb 2024 23:03:42 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87549b73512dc078a9fd0676c455016434712b987ebca91fc86e53034be1a13`  
		Last Modified: Fri, 16 Feb 2024 01:50:10 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e877f62117e03a836f99aced278343c1f674e699f027fa7e865634baba5fc7b`  
		Last Modified: Fri, 16 Feb 2024 01:50:10 GMT  
		Size: 5.6 MB (5649877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e31e9a7630b49d8c1f1e0e5e2cacfd56a8e75fa970d20d0d5ec22573a60959`  
		Last Modified: Fri, 16 Feb 2024 01:50:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242764cd2769225841e0c561adfb3e1371d47f7af0112515d9fb739cf778dda0`  
		Last Modified: Fri, 16 Feb 2024 01:50:11 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053822b225f3d3340812c75e244fa18029d7a95a39932299f445e0e09c461bcd`  
		Last Modified: Fri, 16 Feb 2024 01:50:12 GMT  
		Size: 87.3 MB (87267509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4cebe0a8923eb0675342f4ee5bd77676488df835790accd83f75f71cfb06e`  
		Last Modified: Fri, 16 Feb 2024 01:50:11 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8b8e7f51d342f2c038eab5f3906fb510de4e96164e12a971483a80438ae572`  
		Last Modified: Fri, 16 Feb 2024 01:50:12 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9d12ce6fadf353e550cd8b9eb64384d39181d9d82395ae2c96f197d3b54f4c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef264f9ce404ab1da86ff0e1885074b9ec457a78cb48b89aff22af67792649f`

```dockerfile
```

-	Layers:
	-	`sha256:57437c15adc7f8ac41bbff0018943e32c826758bff08566f5de4e89bb16582c0`  
		Last Modified: Fri, 16 Feb 2024 01:50:10 GMT  
		Size: 4.0 MB (3977923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4bb09d0d99d143ea050d2a990a72891368391c0e2dc053a682b6d1ff95dd7e`  
		Last Modified: Fri, 16 Feb 2024 01:50:10 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3e0d1d01c136247d0e76ffdf1008bfe92e9b804a6a7c62d9b8c500742c938940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a4e712dba4f4a9d48c85023c2dff04c01227ead341672987f9f5a519cac0b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 11 Feb 2024 23:03:42 GMT
ARG RELEASE
# Sun, 11 Feb 2024 23:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 11 Feb 2024 23:03:42 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
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
	-	`sha256:76ab93157f6e3acb9d05d400f66eba27791d96ad3487e8ed9cdbe3d59f365ab8`  
		Last Modified: Fri, 16 Feb 2024 19:01:14 GMT  
		Size: 84.0 MB (84031635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfd34f6f34a563edec447ca299ec8732194c10bd1684db3b655b7caf881817b`  
		Last Modified: Fri, 16 Feb 2024 19:01:11 GMT  
		Size: 3.6 KB (3618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44c93ae7057bcced60a0c8369dd98a0d24241644c66d6a76fd7a69116af0c20`  
		Last Modified: Fri, 16 Feb 2024 19:01:11 GMT  
		Size: 8.3 KB (8256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:84a6a2b0c3d84ad24a2d758bfcf328269d32265c7d28044a77430ea1e93d3cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea77e7a9ea62c392d6882a7a8f7963314cdb5662dfb04fb2e83e26ca4880b34`

```dockerfile
```

-	Layers:
	-	`sha256:5fb13538448913317fdf760f865262a24a7f16f0dd0b3e832dad22586e32bb20`  
		Last Modified: Fri, 16 Feb 2024 19:01:11 GMT  
		Size: 4.0 MB (3983671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf2fd0e7da21d99c455cfed079e90b89d0d57a72ff5be4d0dfc572d0998e5b4`  
		Last Modified: Fri, 16 Feb 2024 19:01:11 GMT  
		Size: 31.0 KB (30992 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b83675fb571280a4f2e2b6f58dfb5657715466ce9dc5f466d7ef8277f137f042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130560336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46c6ab40192568db27944f4338b051e1cf14e4de83aa4f22377f36ad78e27ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 11 Feb 2024 23:03:42 GMT
ARG RELEASE
# Sun, 11 Feb 2024 23:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 11 Feb 2024 23:03:42 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe3be62365843aee2bdf1f45dc0bf2b8f2ed648b890fd19e1c7b7c70060b619`  
		Last Modified: Fri, 16 Feb 2024 18:50:01 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e56ec5ffcfa9b7d078d4d3e35a14bb065cefb553ac185ac30ce7b37fd9ea1`  
		Last Modified: Fri, 16 Feb 2024 18:50:02 GMT  
		Size: 6.1 MB (6082125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd21739fa35b4d46c16c0a78b7b3063f2fc9fe3dcd4f0dae212961444645d0`  
		Last Modified: Fri, 16 Feb 2024 18:50:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152343e6649fbb25af2a2f3e8ed313e2b183d10bab17b2d6f03d46b4a69d51b1`  
		Last Modified: Fri, 16 Feb 2024 18:51:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274a7d6cb882da51db08fb3638a33c314054c33583bfc29e82889194932a005`  
		Last Modified: Fri, 16 Feb 2024 18:51:52 GMT  
		Size: 90.0 MB (89960950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66120997c39eb66fa9234925965d32fcff046f32b2dd00ca46c881d2ef247d47`  
		Last Modified: Fri, 16 Feb 2024 18:51:49 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dc00c4627cc014cae142b18d7535ec76516162c2d3c514dcd5539d4135b404`  
		Last Modified: Fri, 16 Feb 2024 18:51:49 GMT  
		Size: 8.3 KB (8252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7d269195bd295f12cf1add238e6814c11131931cd487ae6d86f2cf1b01860d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bc1fdd4f589bbfb3988c880d1f1731ff70fb46cab47d0fe61359a9f36186f`

```dockerfile
```

-	Layers:
	-	`sha256:2010e3a7262e297358610ebf9e690f0602ef9549f7da92c7c756e86b46b9086c`  
		Last Modified: Fri, 16 Feb 2024 18:51:49 GMT  
		Size: 4.0 MB (3985594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ce40402b836e47dbb02a017a9be415626da8243528a7b3624ffcca2d3de1401`  
		Last Modified: Fri, 16 Feb 2024 18:51:49 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:daaba61f9ac41b66e6f1b9dfbf4edfbe1e1edb96da8ac87152d5a9666b7c53e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121304270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487ab23c70d4050235a34cbc59c71e0d375a472af70bd3b34230999abd48fc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d3f6e9c064408f6bf66f03647e17b172da495eb31a475378dfc58729503e`  
		Last Modified: Tue, 13 Feb 2024 20:55:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5860ced949db6af4b08925e2b18084c343d307699ac365f3f8d68211efca2d`  
		Last Modified: Tue, 13 Feb 2024 20:55:26 GMT  
		Size: 87.7 MB (87726446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d56e334859ce3b95b090955786ccd57990412568e3273330332afebfc38600`  
		Last Modified: Tue, 13 Feb 2024 20:55:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b08caea71cd92f22cf8a0ea40f6b052ce4416276206ef5857956d9fe407760`  
		Last Modified: Tue, 13 Feb 2024 20:55:24 GMT  
		Size: 8.2 KB (8248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:19bd8b380f038d2018ae739809e403a65de59f78db24cfcd0e469ce3666b39ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3521dc8b7be38d4f4cd7a666546778c30dc94c0dbb403ca5a63da88c32489807`

```dockerfile
```

-	Layers:
	-	`sha256:66a8a068f36d2c898f1701f3576f4b6713fdadddf113edbb236cb7692c90b2aa`  
		Last Modified: Tue, 13 Feb 2024 20:55:25 GMT  
		Size: 4.0 MB (3957660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:261e96c719e8cca70abd03c7e23500c6fbc41886e12c3f9595913b1f472230f9`  
		Last Modified: Tue, 13 Feb 2024 20:55:24 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
