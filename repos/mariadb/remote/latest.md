## `mariadb:latest`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:ed4d9a7e3bb408ec262c605fda9230936e61e66464e7eb32f8bda9cdcd6079b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127205438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d462573d8688665ea676252d2c2609f9ff748ee0d9b53744bcc358fb511a7438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:30:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:30:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:30:13 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:30:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:30:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:30:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:30:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:30:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:31:27 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:31:27 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:31:28 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:31:28 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:31:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:31:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:31:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:31:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:31:53 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb9a1b1379d382a02f804f895972f9c2ba01f908768010c823ed2648b6132f3`  
		Last Modified: Fri, 07 Jan 2022 03:35:32 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5c95406850b1bb9ecafc53b866c4687faf64a80a163ee76387a78e94687d1c`  
		Last Modified: Fri, 07 Jan 2022 03:35:32 GMT  
		Size: 5.5 MB (5488763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa48d8b47ec1288c6e337e7619b2838ba3e8bdfdcbdd16426e68ca3c084f0844`  
		Last Modified: Fri, 07 Jan 2022 03:35:31 GMT  
		Size: 3.6 MB (3585336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf1feb44ac3575e779ad11734f6ad167be8cb23bec30bc33d24f7cc6d68e003`  
		Last Modified: Fri, 07 Jan 2022 03:35:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5de7784a0f129e0ed2000cd89777c96669e93c011dc882adf95cd30dc7bf8c`  
		Last Modified: Fri, 07 Jan 2022 03:35:29 GMT  
		Size: 2.3 MB (2273175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8724b8a281aa18cd8f3a7588a789ef20b4b22078def2d60c911e4603a5cdb34`  
		Last Modified: Fri, 07 Jan 2022 03:35:30 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7c3f612d63188e19d915944e25b812bbc88d15bc49478985c6f2b8e231aad`  
		Last Modified: Fri, 07 Jan 2022 03:35:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b09b59e8891ac12c663f8704568aedfda1460db5b9de8e66cc54b2d99ffe59`  
		Last Modified: Fri, 07 Jan 2022 03:36:10 GMT  
		Size: 87.3 MB (87281406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bc3a6b0a9481270a9f59536cabe175fbcc85ef5e175594014e624a4bfbc59b`  
		Last Modified: Fri, 07 Jan 2022 03:35:57 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3ad67ebc689d8b27aa7833a709b6c9f53114546aea3ca3fd5097eab42eefadac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124378829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11ffe318384cb4670eac288156b5ea311f950f063936d5ecf353d34ac848d76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:42:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:42:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:42:47 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:43:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:43:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:43:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:43:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:43:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:44:16 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:44:17 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:44:18 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:44:19 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:44:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:44:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:44:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:44:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:44:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:44:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:44:59 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849321314592efe8eaf10df11072fca76e40f268a2eaa1d764975341c69883c0`  
		Last Modified: Fri, 07 Jan 2022 03:50:24 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b057898d0a8fb18b2a6e4155fd0455277a127fab5912ce5f7844f5a09d59f44`  
		Last Modified: Fri, 07 Jan 2022 03:50:24 GMT  
		Size: 5.3 MB (5320874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5657a3d021aa7f224cf84074d039bfd63526a987ea361c185e21f1a54adffcdc`  
		Last Modified: Fri, 07 Jan 2022 03:50:24 GMT  
		Size: 3.4 MB (3370656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20e9c5cba16b1d2838bd25dd4f808694ffd769fa1193213eabcf3fd13ca94aa`  
		Last Modified: Fri, 07 Jan 2022 03:50:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411d77306ea00e4d5ff0b2cff80f6861e5e555068852cb574ace66ff1efc30b8`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 2.2 MB (2203751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e227c564efcd089bd50fe1d9c797bb7c23f5dd544625a6d763a5446e1d1b43b`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e280f92ec1876b4c614e73b4ac312006551c1983d6d6d1d9cced5bd49e2fb`  
		Last Modified: Fri, 07 Jan 2022 03:50:52 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405ac22bead3574365a6d128d5bb6c4fa0412d8ebd97d739c79c6b3b6e52f0d0`  
		Last Modified: Fri, 07 Jan 2022 03:51:05 GMT  
		Size: 86.3 MB (86302220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9dcc6cd4e2e2f0c6b057cf8ef14f11ef8932f9fb9b3e0a6e5e4548a5fd932a`  
		Last Modified: Fri, 07 Jan 2022 03:50:52 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:41faa0d72961963a9ae4f01185920e09f01e29298cb68e9ff964508fc396067a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137785680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b0f214975a49dc93ddd246e0fd8e0027656dfc91a5cf5216763e2470113e08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:34:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:35:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:35:13 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:35:58 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:36:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:36:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:36:30 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:36:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:39:02 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:39:03 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 03:39:05 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:39:06 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 03:39:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:39:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:40:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:40:57 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:40:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:41:01 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:41:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4091b8bb8c47866846e7995ccf1da82c3aa80b074d08a7d80b89c5752cd6cdde`  
		Last Modified: Fri, 07 Jan 2022 03:52:55 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40da232e13e286b82a5c8f2d969b069ce9ff76e67d9b43e494f2b648267dcd`  
		Last Modified: Fri, 07 Jan 2022 03:52:55 GMT  
		Size: 6.7 MB (6667554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c350ae8e3d175cf91efe886ac4e89ae5fbaded80642980062682b91bd122d92`  
		Last Modified: Fri, 07 Jan 2022 03:52:55 GMT  
		Size: 3.7 MB (3672875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25d84b89fdb0bfa431f08ce835836bbd8aec07f424cda2f4d3d0b69eee7302`  
		Last Modified: Fri, 07 Jan 2022 03:52:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4aeec1caf65530a8e76996b27fdbe7a93a0a43b114621f077c4ce3c0fd511c5`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 2.6 MB (2568908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41feb239d1090e6a6003ed0d1bc1d2bd5ad2178d4a92ee3816cae81835c1a3e4`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348e8cb06c0d9b5c0446ac943e5928fb69a37553bab25c43d1326b8e63d1f2e9`  
		Last Modified: Fri, 07 Jan 2022 03:53:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271d7b0ec460dc1c18017800a90869a370b4fcb377740884070136326eb9ccb2`  
		Last Modified: Fri, 07 Jan 2022 03:53:48 GMT  
		Size: 91.6 MB (91579113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f6c6467339798f302ceb133632e7acb03b46214c32e1fb31e401296e708a48`  
		Last Modified: Fri, 07 Jan 2022 03:53:30 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:4354ddd19fe019085fd4bdaaf713d83ae43beb692a99ca0a2fffd9f7524e5b45
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126214292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df0bedfb4336254a4be7c22f1e9de74f1badf9a83dd0af569ee97d218c9cfaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:35:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 02:35:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:35:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 02:36:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 02:36:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 02:36:07 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:36:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 02:36:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 02:36:54 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 02:36:54 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 07 Jan 2022 02:36:55 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 02:36:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Fri, 07 Jan 2022 02:36:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:36:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:37:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:37:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:37:29 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:37:29 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:37:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f86a1ecc18991dcf3e67d3fa546e9f6cd0ce2a82a8ab5e4c1a18454d251561`  
		Last Modified: Fri, 07 Jan 2022 02:38:47 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e55aa6d4e377745f7680583e1d80b4fe596b012f8d7d4d448c461cd039d39b0`  
		Last Modified: Fri, 07 Jan 2022 02:38:48 GMT  
		Size: 5.4 MB (5381045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21350327ab5e8863399d01173b168d269325a4b6d051363b2f1f6afca428b40`  
		Last Modified: Fri, 07 Jan 2022 02:38:47 GMT  
		Size: 3.2 MB (3244640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e229a56e4589b4e6219ee404f79535dd359ea1519fa63154191e60c2af364`  
		Last Modified: Fri, 07 Jan 2022 02:38:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d926bdb1a7f3ba66de3c6e135aa5c4c6bcec6a5581251658e4100227275086b`  
		Last Modified: Fri, 07 Jan 2022 02:38:46 GMT  
		Size: 2.2 MB (2185670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4598ff63a597a4c320ca9fed567120e4babb6624ef94825e2f76553d05e2425`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5ce2a6eedbadc4111b8d2d6bfdcd95141e3e3d8861c956df4bf92890febc49`  
		Last Modified: Fri, 07 Jan 2022 02:39:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943024f5ecfef7413b7192bee3e9f484c7cc5169de49f65b247eb4ce6fca435d`  
		Last Modified: Fri, 07 Jan 2022 02:39:22 GMT  
		Size: 88.3 MB (88271606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a90e41db20c844f7ade17ea9b50c7b8021d72e99bddce80ec606c2a4310349`  
		Last Modified: Fri, 07 Jan 2022 02:39:09 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
