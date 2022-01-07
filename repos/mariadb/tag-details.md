<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.41`](#mariadb10241)
-	[`mariadb:10.2.41-bionic`](#mariadb10241-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.32`](#mariadb10332)
-	[`mariadb:10.3.32-focal`](#mariadb10332-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.22`](#mariadb10422)
-	[`mariadb:10.4.22-focal`](#mariadb10422-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.13`](#mariadb10513)
-	[`mariadb:10.5.13-focal`](#mariadb10513-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.5`](#mariadb1065)
-	[`mariadb:10.6.5-focal`](#mariadb1065-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.1`](#mariadb1071)
-	[`mariadb:10.7.1-focal`](#mariadb1071-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

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

### `mariadb:10` - linux; arm64 variant v8

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

### `mariadb:10` - linux; ppc64le

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

### `mariadb:10` - linux; s390x

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

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

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

### `mariadb:10-focal` - linux; arm64 variant v8

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

### `mariadb:10-focal` - linux; ppc64le

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

### `mariadb:10-focal` - linux; s390x

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

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:62f9ccdcb7962b385b7ac4715d99a6fd69fe653afcd036c638c94e1d5e2cfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:2b6d57fd12311858bb3914a444da942fcb68a69fb58b4e22228795b567ab8773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109368012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba75a3daccc7da52963e1d6191eaf341086d6f1805ceed4bf826cf5327c9102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:33:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:33:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:33:46 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:33:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:34:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:34:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:34:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:34:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:34:51 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:34:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:34:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:34:53 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:34:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a154688034c5c276e6d12e0b251bf453265cc25a88c20ad7962eb0cb82b706b`  
		Last Modified: Fri, 07 Jan 2022 03:38:12 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4558069aa5016b3f9742407b1aac60b61ce9bb83c13544e379584f2fe57361`  
		Last Modified: Fri, 07 Jan 2022 03:38:11 GMT  
		Size: 4.8 MB (4813672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f47b1cf9b8080b7ebbc7d360e21dbef4d24a252d2971be582825762b1cb06b`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 3.6 MB (3553551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988606574463620c5bf37cf08a89bb23f3b3334c6ea34c3e1b86086d8a5bd2e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc122fdb362ed245ac54864f106e39f8d4202d9db222fc05646e25363295f16e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 1.6 MB (1584008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038dfea729d26b221c67e68d89807e283c19f74ce922ad3479e19400ef2f0b7d`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da96ca1ec9f45dca791f13120e42984b1e16b9f0da0f931c7eca817ba645b9c`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71436fc1053a8bb4f525df24f04499ed8089b269191e1305cfed282c78af01`  
		Last Modified: Fri, 07 Jan 2022 03:38:18 GMT  
		Size: 72.7 MB (72698482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d382beb7c039b957f4373b4a53cc4fb7891b93197092f431d0cc2c263ec65`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc114e1f845a5ce74ff59ca1c8932ae38c3a7c0dcad773ae9bb3f4ba0ac83393`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d573b330b8bb46204a4ec4ebd828353b23660f12248dbd509dd4e48492d100dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14579c4cfca35a7a2bf47812dd7d7dbeb2ec9adad7627fb8a43f149952e86af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:01 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:48:18 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:48:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:48:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:48:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:48:37 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:38 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:39 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:40 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:48:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:49:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:49:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:49:16 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:49:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:49:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:49:18 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589029f3445243b17f31b5666d58a5e0a0c3083424fb90b69b26525078d26b0f`  
		Last Modified: Fri, 07 Jan 2022 03:53:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfda350e0c72be321f5307d232804d46ddb689c7446139ae18ce89a33bad54a1`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 4.3 MB (4261614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fa958c8d8e16b85b10ac8194881e1ed6bde65b4364f54e69b65b7f31c155c`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 3.2 MB (3207348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2519e0202871d5a62527bd5bfeed4ee6381bf8787a15a2baa6ad314622a94f2`  
		Last Modified: Fri, 07 Jan 2022 03:53:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4520147e3d7bd785fe189ce65dd9e0914e8db69f7bbcf088bb0c09eef76e62cf`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 1.5 MB (1529545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcdddeb3dc445ea0f461484d44dd032d6b5b08711d60e8a5517724c2aac2746`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.1 KB (5146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5395e54035125128b9a352283a6b8bbbf8677977e2ba8469c8e984e78eb13f6`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df69d87130c61e4f1bbe4542cedd1ad369404845f52367c25108c79ee1311d5`  
		Last Modified: Fri, 07 Jan 2022 03:53:23 GMT  
		Size: 71.5 MB (71495872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18bf635e4cd5b0a5114758bacea82525a8f95cb474ad147f7fd8a8366392384`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde01f7fa4387c64e92a25797499c51a957cfc1a079aea7bd5e2965d57395970`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bcfa2fb9208a2566b03a350687637eacb8e829e8c688df899ee1d39b3b2b2b54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117697816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5032f4e3193cb867cd19d612ab091a8db506f3e2a18c6de8cc262abcc58c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:32 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:33 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:49:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:49:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:49:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:49:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:49:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:49:48 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:49 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:51 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:52 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:49:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:51:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:51:28 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:51:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:51:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:51:37 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:51:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84119375dfbc674e0c0ece270da8dcb2366630bf7e01a091c30e04cabeeb537f`  
		Last Modified: Fri, 07 Jan 2022 03:56:23 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f911761bd6ab67ea4cc9016ca6595f70042cd2601889de69ca2aed1bcd1df1`  
		Last Modified: Fri, 07 Jan 2022 03:56:22 GMT  
		Size: 5.6 MB (5630246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45277053732e4a477be62347cb5b8ebff6fe6f0db02ae79829a1d6d133c99dae`  
		Last Modified: Fri, 07 Jan 2022 03:56:21 GMT  
		Size: 3.5 MB (3533382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9593e4638ed9f5b4846781d7747628f3000acddbf7d25ffb1446cda9fb7961ff`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1055c951e356812cbdbf23028b34cd7430d5685944fc493790c92b638ebb29`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 1.9 MB (1936828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08cdb0d7858d83faa434a861797a9509068fcf53f527a7bcbf71dd04ebee83`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 5.2 KB (5169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418fa81a63bb2220e9af6988b5271bfbd73f19a748ca2fbee6345286fd0b931`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8374bdd691e0d530ec8e5c6885e47054484632e1e18bed6fe6c5697027b03a9`  
		Last Modified: Fri, 07 Jan 2022 03:56:33 GMT  
		Size: 76.2 MB (76151741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f742e2adfe1b0d49a6bc74aa1bbd23f93ead62f3ae3a1d1df21642d06e6224`  
		Last Modified: Fri, 07 Jan 2022 03:56:18 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b9423abcdeb37c8e2b5496bd8c3a65eb46e34e6a0ab46044ffc043a5635fbc`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:62f9ccdcb7962b385b7ac4715d99a6fd69fe653afcd036c638c94e1d5e2cfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:2b6d57fd12311858bb3914a444da942fcb68a69fb58b4e22228795b567ab8773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109368012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba75a3daccc7da52963e1d6191eaf341086d6f1805ceed4bf826cf5327c9102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:33:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:33:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:33:46 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:33:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:34:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:34:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:34:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:34:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:34:51 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:34:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:34:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:34:53 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:34:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a154688034c5c276e6d12e0b251bf453265cc25a88c20ad7962eb0cb82b706b`  
		Last Modified: Fri, 07 Jan 2022 03:38:12 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4558069aa5016b3f9742407b1aac60b61ce9bb83c13544e379584f2fe57361`  
		Last Modified: Fri, 07 Jan 2022 03:38:11 GMT  
		Size: 4.8 MB (4813672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f47b1cf9b8080b7ebbc7d360e21dbef4d24a252d2971be582825762b1cb06b`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 3.6 MB (3553551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988606574463620c5bf37cf08a89bb23f3b3334c6ea34c3e1b86086d8a5bd2e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc122fdb362ed245ac54864f106e39f8d4202d9db222fc05646e25363295f16e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 1.6 MB (1584008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038dfea729d26b221c67e68d89807e283c19f74ce922ad3479e19400ef2f0b7d`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da96ca1ec9f45dca791f13120e42984b1e16b9f0da0f931c7eca817ba645b9c`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71436fc1053a8bb4f525df24f04499ed8089b269191e1305cfed282c78af01`  
		Last Modified: Fri, 07 Jan 2022 03:38:18 GMT  
		Size: 72.7 MB (72698482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d382beb7c039b957f4373b4a53cc4fb7891b93197092f431d0cc2c263ec65`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc114e1f845a5ce74ff59ca1c8932ae38c3a7c0dcad773ae9bb3f4ba0ac83393`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d573b330b8bb46204a4ec4ebd828353b23660f12248dbd509dd4e48492d100dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14579c4cfca35a7a2bf47812dd7d7dbeb2ec9adad7627fb8a43f149952e86af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:01 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:48:18 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:48:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:48:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:48:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:48:37 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:38 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:39 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:40 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:48:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:49:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:49:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:49:16 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:49:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:49:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:49:18 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589029f3445243b17f31b5666d58a5e0a0c3083424fb90b69b26525078d26b0f`  
		Last Modified: Fri, 07 Jan 2022 03:53:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfda350e0c72be321f5307d232804d46ddb689c7446139ae18ce89a33bad54a1`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 4.3 MB (4261614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fa958c8d8e16b85b10ac8194881e1ed6bde65b4364f54e69b65b7f31c155c`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 3.2 MB (3207348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2519e0202871d5a62527bd5bfeed4ee6381bf8787a15a2baa6ad314622a94f2`  
		Last Modified: Fri, 07 Jan 2022 03:53:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4520147e3d7bd785fe189ce65dd9e0914e8db69f7bbcf088bb0c09eef76e62cf`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 1.5 MB (1529545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcdddeb3dc445ea0f461484d44dd032d6b5b08711d60e8a5517724c2aac2746`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.1 KB (5146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5395e54035125128b9a352283a6b8bbbf8677977e2ba8469c8e984e78eb13f6`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df69d87130c61e4f1bbe4542cedd1ad369404845f52367c25108c79ee1311d5`  
		Last Modified: Fri, 07 Jan 2022 03:53:23 GMT  
		Size: 71.5 MB (71495872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18bf635e4cd5b0a5114758bacea82525a8f95cb474ad147f7fd8a8366392384`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde01f7fa4387c64e92a25797499c51a957cfc1a079aea7bd5e2965d57395970`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bcfa2fb9208a2566b03a350687637eacb8e829e8c688df899ee1d39b3b2b2b54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117697816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5032f4e3193cb867cd19d612ab091a8db506f3e2a18c6de8cc262abcc58c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:32 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:33 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:49:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:49:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:49:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:49:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:49:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:49:48 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:49 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:51 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:52 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:49:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:51:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:51:28 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:51:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:51:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:51:37 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:51:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84119375dfbc674e0c0ece270da8dcb2366630bf7e01a091c30e04cabeeb537f`  
		Last Modified: Fri, 07 Jan 2022 03:56:23 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f911761bd6ab67ea4cc9016ca6595f70042cd2601889de69ca2aed1bcd1df1`  
		Last Modified: Fri, 07 Jan 2022 03:56:22 GMT  
		Size: 5.6 MB (5630246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45277053732e4a477be62347cb5b8ebff6fe6f0db02ae79829a1d6d133c99dae`  
		Last Modified: Fri, 07 Jan 2022 03:56:21 GMT  
		Size: 3.5 MB (3533382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9593e4638ed9f5b4846781d7747628f3000acddbf7d25ffb1446cda9fb7961ff`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1055c951e356812cbdbf23028b34cd7430d5685944fc493790c92b638ebb29`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 1.9 MB (1936828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08cdb0d7858d83faa434a861797a9509068fcf53f527a7bcbf71dd04ebee83`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 5.2 KB (5169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418fa81a63bb2220e9af6988b5271bfbd73f19a748ca2fbee6345286fd0b931`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8374bdd691e0d530ec8e5c6885e47054484632e1e18bed6fe6c5697027b03a9`  
		Last Modified: Fri, 07 Jan 2022 03:56:33 GMT  
		Size: 76.2 MB (76151741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f742e2adfe1b0d49a6bc74aa1bbd23f93ead62f3ae3a1d1df21642d06e6224`  
		Last Modified: Fri, 07 Jan 2022 03:56:18 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b9423abcdeb37c8e2b5496bd8c3a65eb46e34e6a0ab46044ffc043a5635fbc`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41`

```console
$ docker pull mariadb@sha256:62f9ccdcb7962b385b7ac4715d99a6fd69fe653afcd036c638c94e1d5e2cfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41` - linux; amd64

```console
$ docker pull mariadb@sha256:2b6d57fd12311858bb3914a444da942fcb68a69fb58b4e22228795b567ab8773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109368012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba75a3daccc7da52963e1d6191eaf341086d6f1805ceed4bf826cf5327c9102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:33:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:33:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:33:46 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:33:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:34:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:34:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:34:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:34:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:34:51 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:34:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:34:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:34:53 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:34:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a154688034c5c276e6d12e0b251bf453265cc25a88c20ad7962eb0cb82b706b`  
		Last Modified: Fri, 07 Jan 2022 03:38:12 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4558069aa5016b3f9742407b1aac60b61ce9bb83c13544e379584f2fe57361`  
		Last Modified: Fri, 07 Jan 2022 03:38:11 GMT  
		Size: 4.8 MB (4813672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f47b1cf9b8080b7ebbc7d360e21dbef4d24a252d2971be582825762b1cb06b`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 3.6 MB (3553551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988606574463620c5bf37cf08a89bb23f3b3334c6ea34c3e1b86086d8a5bd2e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc122fdb362ed245ac54864f106e39f8d4202d9db222fc05646e25363295f16e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 1.6 MB (1584008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038dfea729d26b221c67e68d89807e283c19f74ce922ad3479e19400ef2f0b7d`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da96ca1ec9f45dca791f13120e42984b1e16b9f0da0f931c7eca817ba645b9c`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71436fc1053a8bb4f525df24f04499ed8089b269191e1305cfed282c78af01`  
		Last Modified: Fri, 07 Jan 2022 03:38:18 GMT  
		Size: 72.7 MB (72698482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d382beb7c039b957f4373b4a53cc4fb7891b93197092f431d0cc2c263ec65`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc114e1f845a5ce74ff59ca1c8932ae38c3a7c0dcad773ae9bb3f4ba0ac83393`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d573b330b8bb46204a4ec4ebd828353b23660f12248dbd509dd4e48492d100dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14579c4cfca35a7a2bf47812dd7d7dbeb2ec9adad7627fb8a43f149952e86af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:01 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:48:18 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:48:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:48:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:48:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:48:37 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:38 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:39 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:40 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:48:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:49:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:49:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:49:16 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:49:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:49:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:49:18 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589029f3445243b17f31b5666d58a5e0a0c3083424fb90b69b26525078d26b0f`  
		Last Modified: Fri, 07 Jan 2022 03:53:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfda350e0c72be321f5307d232804d46ddb689c7446139ae18ce89a33bad54a1`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 4.3 MB (4261614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fa958c8d8e16b85b10ac8194881e1ed6bde65b4364f54e69b65b7f31c155c`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 3.2 MB (3207348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2519e0202871d5a62527bd5bfeed4ee6381bf8787a15a2baa6ad314622a94f2`  
		Last Modified: Fri, 07 Jan 2022 03:53:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4520147e3d7bd785fe189ce65dd9e0914e8db69f7bbcf088bb0c09eef76e62cf`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 1.5 MB (1529545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcdddeb3dc445ea0f461484d44dd032d6b5b08711d60e8a5517724c2aac2746`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.1 KB (5146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5395e54035125128b9a352283a6b8bbbf8677977e2ba8469c8e984e78eb13f6`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df69d87130c61e4f1bbe4542cedd1ad369404845f52367c25108c79ee1311d5`  
		Last Modified: Fri, 07 Jan 2022 03:53:23 GMT  
		Size: 71.5 MB (71495872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18bf635e4cd5b0a5114758bacea82525a8f95cb474ad147f7fd8a8366392384`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde01f7fa4387c64e92a25797499c51a957cfc1a079aea7bd5e2965d57395970`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bcfa2fb9208a2566b03a350687637eacb8e829e8c688df899ee1d39b3b2b2b54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117697816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5032f4e3193cb867cd19d612ab091a8db506f3e2a18c6de8cc262abcc58c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:32 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:33 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:49:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:49:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:49:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:49:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:49:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:49:48 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:49 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:51 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:52 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:49:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:51:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:51:28 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:51:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:51:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:51:37 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:51:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84119375dfbc674e0c0ece270da8dcb2366630bf7e01a091c30e04cabeeb537f`  
		Last Modified: Fri, 07 Jan 2022 03:56:23 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f911761bd6ab67ea4cc9016ca6595f70042cd2601889de69ca2aed1bcd1df1`  
		Last Modified: Fri, 07 Jan 2022 03:56:22 GMT  
		Size: 5.6 MB (5630246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45277053732e4a477be62347cb5b8ebff6fe6f0db02ae79829a1d6d133c99dae`  
		Last Modified: Fri, 07 Jan 2022 03:56:21 GMT  
		Size: 3.5 MB (3533382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9593e4638ed9f5b4846781d7747628f3000acddbf7d25ffb1446cda9fb7961ff`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1055c951e356812cbdbf23028b34cd7430d5685944fc493790c92b638ebb29`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 1.9 MB (1936828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08cdb0d7858d83faa434a861797a9509068fcf53f527a7bcbf71dd04ebee83`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 5.2 KB (5169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418fa81a63bb2220e9af6988b5271bfbd73f19a748ca2fbee6345286fd0b931`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8374bdd691e0d530ec8e5c6885e47054484632e1e18bed6fe6c5697027b03a9`  
		Last Modified: Fri, 07 Jan 2022 03:56:33 GMT  
		Size: 76.2 MB (76151741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f742e2adfe1b0d49a6bc74aa1bbd23f93ead62f3ae3a1d1df21642d06e6224`  
		Last Modified: Fri, 07 Jan 2022 03:56:18 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b9423abcdeb37c8e2b5496bd8c3a65eb46e34e6a0ab46044ffc043a5635fbc`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41-bionic`

```console
$ docker pull mariadb@sha256:62f9ccdcb7962b385b7ac4715d99a6fd69fe653afcd036c638c94e1d5e2cfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:2b6d57fd12311858bb3914a444da942fcb68a69fb58b4e22228795b567ab8773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109368012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba75a3daccc7da52963e1d6191eaf341086d6f1805ceed4bf826cf5327c9102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:33:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:33:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:33:46 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:33:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:34:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:34:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:34:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:34:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:34:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:34:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:34:51 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:34:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:34:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:34:53 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:34:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a154688034c5c276e6d12e0b251bf453265cc25a88c20ad7962eb0cb82b706b`  
		Last Modified: Fri, 07 Jan 2022 03:38:12 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4558069aa5016b3f9742407b1aac60b61ce9bb83c13544e379584f2fe57361`  
		Last Modified: Fri, 07 Jan 2022 03:38:11 GMT  
		Size: 4.8 MB (4813672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f47b1cf9b8080b7ebbc7d360e21dbef4d24a252d2971be582825762b1cb06b`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 3.6 MB (3553551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988606574463620c5bf37cf08a89bb23f3b3334c6ea34c3e1b86086d8a5bd2e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc122fdb362ed245ac54864f106e39f8d4202d9db222fc05646e25363295f16e`  
		Last Modified: Fri, 07 Jan 2022 03:38:10 GMT  
		Size: 1.6 MB (1584008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038dfea729d26b221c67e68d89807e283c19f74ce922ad3479e19400ef2f0b7d`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da96ca1ec9f45dca791f13120e42984b1e16b9f0da0f931c7eca817ba645b9c`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71436fc1053a8bb4f525df24f04499ed8089b269191e1305cfed282c78af01`  
		Last Modified: Fri, 07 Jan 2022 03:38:18 GMT  
		Size: 72.7 MB (72698482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d382beb7c039b957f4373b4a53cc4fb7891b93197092f431d0cc2c263ec65`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc114e1f845a5ce74ff59ca1c8932ae38c3a7c0dcad773ae9bb3f4ba0ac83393`  
		Last Modified: Fri, 07 Jan 2022 03:38:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d573b330b8bb46204a4ec4ebd828353b23660f12248dbd509dd4e48492d100dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14579c4cfca35a7a2bf47812dd7d7dbeb2ec9adad7627fb8a43f149952e86af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:01 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:48:18 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:48:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:48:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:48:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:48:37 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:38 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:48:39 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:40 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:48:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:48:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:49:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:49:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:49:16 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:49:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:49:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:49:18 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589029f3445243b17f31b5666d58a5e0a0c3083424fb90b69b26525078d26b0f`  
		Last Modified: Fri, 07 Jan 2022 03:53:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfda350e0c72be321f5307d232804d46ddb689c7446139ae18ce89a33bad54a1`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 4.3 MB (4261614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fa958c8d8e16b85b10ac8194881e1ed6bde65b4364f54e69b65b7f31c155c`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 3.2 MB (3207348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2519e0202871d5a62527bd5bfeed4ee6381bf8787a15a2baa6ad314622a94f2`  
		Last Modified: Fri, 07 Jan 2022 03:53:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4520147e3d7bd785fe189ce65dd9e0914e8db69f7bbcf088bb0c09eef76e62cf`  
		Last Modified: Fri, 07 Jan 2022 03:53:15 GMT  
		Size: 1.5 MB (1529545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcdddeb3dc445ea0f461484d44dd032d6b5b08711d60e8a5517724c2aac2746`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.1 KB (5146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5395e54035125128b9a352283a6b8bbbf8677977e2ba8469c8e984e78eb13f6`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df69d87130c61e4f1bbe4542cedd1ad369404845f52367c25108c79ee1311d5`  
		Last Modified: Fri, 07 Jan 2022 03:53:23 GMT  
		Size: 71.5 MB (71495872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18bf635e4cd5b0a5114758bacea82525a8f95cb474ad147f7fd8a8366392384`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde01f7fa4387c64e92a25797499c51a957cfc1a079aea7bd5e2965d57395970`  
		Last Modified: Fri, 07 Jan 2022 03:53:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bcfa2fb9208a2566b03a350687637eacb8e829e8c688df899ee1d39b3b2b2b54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117697816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5032f4e3193cb867cd19d612ab091a8db506f3e2a18c6de8cc262abcc58c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:47:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 07 Jan 2022 03:48:32 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:48:33 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Jan 2022 03:49:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:49:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:49:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:49:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 07 Jan 2022 03:49:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:49:48 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:49 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 07 Jan 2022 03:49:51 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:52 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Fri, 07 Jan 2022 03:49:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Fri, 07 Jan 2022 03:49:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:51:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:51:28 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:51:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:51:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:51:37 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:51:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84119375dfbc674e0c0ece270da8dcb2366630bf7e01a091c30e04cabeeb537f`  
		Last Modified: Fri, 07 Jan 2022 03:56:23 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f911761bd6ab67ea4cc9016ca6595f70042cd2601889de69ca2aed1bcd1df1`  
		Last Modified: Fri, 07 Jan 2022 03:56:22 GMT  
		Size: 5.6 MB (5630246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45277053732e4a477be62347cb5b8ebff6fe6f0db02ae79829a1d6d133c99dae`  
		Last Modified: Fri, 07 Jan 2022 03:56:21 GMT  
		Size: 3.5 MB (3533382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9593e4638ed9f5b4846781d7747628f3000acddbf7d25ffb1446cda9fb7961ff`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1055c951e356812cbdbf23028b34cd7430d5685944fc493790c92b638ebb29`  
		Last Modified: Fri, 07 Jan 2022 03:56:20 GMT  
		Size: 1.9 MB (1936828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08cdb0d7858d83faa434a861797a9509068fcf53f527a7bcbf71dd04ebee83`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 5.2 KB (5169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418fa81a63bb2220e9af6988b5271bfbd73f19a748ca2fbee6345286fd0b931`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8374bdd691e0d530ec8e5c6885e47054484632e1e18bed6fe6c5697027b03a9`  
		Last Modified: Fri, 07 Jan 2022 03:56:33 GMT  
		Size: 76.2 MB (76151741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f742e2adfe1b0d49a6bc74aa1bbd23f93ead62f3ae3a1d1df21642d06e6224`  
		Last Modified: Fri, 07 Jan 2022 03:56:18 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b9423abcdeb37c8e2b5496bd8c3a65eb46e34e6a0ab46044ffc043a5635fbc`  
		Last Modified: Fri, 07 Jan 2022 03:56:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:dbb112be4b5528c4e90484763a727cfe3e7aa51e4fc1fd15978d2df20293c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:2e0204389c73a586bdf61a650f62c141a78d5b96bb279a795866ace37c967f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4617772994b84f8613aca58ee8d39da122282ace24965f2ac7bf0749232b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:33:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:33:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:33:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:33:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:33:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:33:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:33:34 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:33:34 GMT
CMD ["mysqld"]
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
	-	`sha256:3cdce65765eae87ce83e60819db50817228eba646e3642ab7f48233555b310bf`  
		Last Modified: Fri, 07 Jan 2022 03:37:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4851ef4bc5e2cb09bb262613524fc2d5709fa40d817178e1b66e3dd76cfc8ce8`  
		Last Modified: Fri, 07 Jan 2022 03:37:45 GMT  
		Size: 80.2 MB (80187777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf70d3093517917b3cdaa5b47af4b0b58e0f07fd5797e657d8cd4c0906966b`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b38af63bb41c4fafe6e9f545c39e16b06d69c254b5521f3bde958cfe0ce99`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a0ad0fa40e058d449e5caf47f090004d1f3336cb35b72428443856bbe1a9514
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117609610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b99a4410533bffa6b459825047f617013f9cca710fa4516833f49f1c8e99e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:46:54 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:55 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:56 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:57 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:46:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:35 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:37 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:39 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:40 GMT
CMD ["mysqld"]
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
	-	`sha256:1fe50c036dbc11c01a34966025f1bb13dd02d17d49adce519aa5f3476d6f657d`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3c32c10438dfc9e0ea677fad181e7f0003c745ce68a04bd9f99ca05b7fafb`  
		Last Modified: Fri, 07 Jan 2022 03:52:53 GMT  
		Size: 79.5 MB (79532877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb100408fe5bc48ae21ee3eb03b41c512b9a0112a935f76314a4bf6822f6c5`  
		Last Modified: Fri, 07 Jan 2022 03:52:41 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bc94fe194e8f25c01a2a754e78f55973c1b2b29263125ebe8538857a50a98`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21c85126c6b1b052f6ece4aa553a8cb30b9d73a547817050e21c86c89884f962
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130990969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe75bce261a08b18e6c368d43a5edaa8a707c403a0f53d3ab2d7096c8eff081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:35 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:38 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:42 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:44 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:30 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:32 GMT
CMD ["mysqld"]
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
	-	`sha256:57c6fb78f11a792ad4c8b574f558f217d851c20fa967abf9ed942f00d1b44b66`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711fab5733e2c461a3619c5bf7850b929437cad2936cb023c30815a8dc5a9063`  
		Last Modified: Fri, 07 Jan 2022 03:55:57 GMT  
		Size: 84.8 MB (84784281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4225a61411885ccd66a7492ccdb59fcf5c039ee164cd0d2a4d10f2a1272bd0`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ab642f18817f4ea955bfcf14e679732ab440b7bc84be54b1149ed91bfff98b`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:dbb112be4b5528c4e90484763a727cfe3e7aa51e4fc1fd15978d2df20293c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e0204389c73a586bdf61a650f62c141a78d5b96bb279a795866ace37c967f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4617772994b84f8613aca58ee8d39da122282ace24965f2ac7bf0749232b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:33:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:33:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:33:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:33:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:33:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:33:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:33:34 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:33:34 GMT
CMD ["mysqld"]
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
	-	`sha256:3cdce65765eae87ce83e60819db50817228eba646e3642ab7f48233555b310bf`  
		Last Modified: Fri, 07 Jan 2022 03:37:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4851ef4bc5e2cb09bb262613524fc2d5709fa40d817178e1b66e3dd76cfc8ce8`  
		Last Modified: Fri, 07 Jan 2022 03:37:45 GMT  
		Size: 80.2 MB (80187777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf70d3093517917b3cdaa5b47af4b0b58e0f07fd5797e657d8cd4c0906966b`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b38af63bb41c4fafe6e9f545c39e16b06d69c254b5521f3bde958cfe0ce99`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a0ad0fa40e058d449e5caf47f090004d1f3336cb35b72428443856bbe1a9514
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117609610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b99a4410533bffa6b459825047f617013f9cca710fa4516833f49f1c8e99e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:46:54 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:55 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:56 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:57 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:46:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:35 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:37 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:39 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:40 GMT
CMD ["mysqld"]
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
	-	`sha256:1fe50c036dbc11c01a34966025f1bb13dd02d17d49adce519aa5f3476d6f657d`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3c32c10438dfc9e0ea677fad181e7f0003c745ce68a04bd9f99ca05b7fafb`  
		Last Modified: Fri, 07 Jan 2022 03:52:53 GMT  
		Size: 79.5 MB (79532877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb100408fe5bc48ae21ee3eb03b41c512b9a0112a935f76314a4bf6822f6c5`  
		Last Modified: Fri, 07 Jan 2022 03:52:41 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bc94fe194e8f25c01a2a754e78f55973c1b2b29263125ebe8538857a50a98`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21c85126c6b1b052f6ece4aa553a8cb30b9d73a547817050e21c86c89884f962
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130990969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe75bce261a08b18e6c368d43a5edaa8a707c403a0f53d3ab2d7096c8eff081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:35 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:38 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:42 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:44 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:30 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:32 GMT
CMD ["mysqld"]
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
	-	`sha256:57c6fb78f11a792ad4c8b574f558f217d851c20fa967abf9ed942f00d1b44b66`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711fab5733e2c461a3619c5bf7850b929437cad2936cb023c30815a8dc5a9063`  
		Last Modified: Fri, 07 Jan 2022 03:55:57 GMT  
		Size: 84.8 MB (84784281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4225a61411885ccd66a7492ccdb59fcf5c039ee164cd0d2a4d10f2a1272bd0`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ab642f18817f4ea955bfcf14e679732ab440b7bc84be54b1149ed91bfff98b`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32`

```console
$ docker pull mariadb@sha256:dbb112be4b5528c4e90484763a727cfe3e7aa51e4fc1fd15978d2df20293c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32` - linux; amd64

```console
$ docker pull mariadb@sha256:2e0204389c73a586bdf61a650f62c141a78d5b96bb279a795866ace37c967f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4617772994b84f8613aca58ee8d39da122282ace24965f2ac7bf0749232b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:33:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:33:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:33:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:33:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:33:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:33:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:33:34 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:33:34 GMT
CMD ["mysqld"]
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
	-	`sha256:3cdce65765eae87ce83e60819db50817228eba646e3642ab7f48233555b310bf`  
		Last Modified: Fri, 07 Jan 2022 03:37:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4851ef4bc5e2cb09bb262613524fc2d5709fa40d817178e1b66e3dd76cfc8ce8`  
		Last Modified: Fri, 07 Jan 2022 03:37:45 GMT  
		Size: 80.2 MB (80187777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf70d3093517917b3cdaa5b47af4b0b58e0f07fd5797e657d8cd4c0906966b`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b38af63bb41c4fafe6e9f545c39e16b06d69c254b5521f3bde958cfe0ce99`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a0ad0fa40e058d449e5caf47f090004d1f3336cb35b72428443856bbe1a9514
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117609610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b99a4410533bffa6b459825047f617013f9cca710fa4516833f49f1c8e99e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:46:54 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:55 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:56 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:57 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:46:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:35 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:37 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:39 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:40 GMT
CMD ["mysqld"]
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
	-	`sha256:1fe50c036dbc11c01a34966025f1bb13dd02d17d49adce519aa5f3476d6f657d`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3c32c10438dfc9e0ea677fad181e7f0003c745ce68a04bd9f99ca05b7fafb`  
		Last Modified: Fri, 07 Jan 2022 03:52:53 GMT  
		Size: 79.5 MB (79532877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb100408fe5bc48ae21ee3eb03b41c512b9a0112a935f76314a4bf6822f6c5`  
		Last Modified: Fri, 07 Jan 2022 03:52:41 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bc94fe194e8f25c01a2a754e78f55973c1b2b29263125ebe8538857a50a98`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21c85126c6b1b052f6ece4aa553a8cb30b9d73a547817050e21c86c89884f962
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130990969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe75bce261a08b18e6c368d43a5edaa8a707c403a0f53d3ab2d7096c8eff081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:35 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:38 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:42 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:44 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:30 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:32 GMT
CMD ["mysqld"]
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
	-	`sha256:57c6fb78f11a792ad4c8b574f558f217d851c20fa967abf9ed942f00d1b44b66`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711fab5733e2c461a3619c5bf7850b929437cad2936cb023c30815a8dc5a9063`  
		Last Modified: Fri, 07 Jan 2022 03:55:57 GMT  
		Size: 84.8 MB (84784281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4225a61411885ccd66a7492ccdb59fcf5c039ee164cd0d2a4d10f2a1272bd0`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ab642f18817f4ea955bfcf14e679732ab440b7bc84be54b1149ed91bfff98b`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32-focal`

```console
$ docker pull mariadb@sha256:dbb112be4b5528c4e90484763a727cfe3e7aa51e4fc1fd15978d2df20293c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e0204389c73a586bdf61a650f62c141a78d5b96bb279a795866ace37c967f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4617772994b84f8613aca58ee8d39da122282ace24965f2ac7bf0749232b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:33:03 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:33:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:33:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:33:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:33:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:33:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:33:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:33:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:33:34 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:33:34 GMT
CMD ["mysqld"]
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
	-	`sha256:3cdce65765eae87ce83e60819db50817228eba646e3642ab7f48233555b310bf`  
		Last Modified: Fri, 07 Jan 2022 03:37:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4851ef4bc5e2cb09bb262613524fc2d5709fa40d817178e1b66e3dd76cfc8ce8`  
		Last Modified: Fri, 07 Jan 2022 03:37:45 GMT  
		Size: 80.2 MB (80187777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf70d3093517917b3cdaa5b47af4b0b58e0f07fd5797e657d8cd4c0906966b`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b38af63bb41c4fafe6e9f545c39e16b06d69c254b5521f3bde958cfe0ce99`  
		Last Modified: Fri, 07 Jan 2022 03:37:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a0ad0fa40e058d449e5caf47f090004d1f3336cb35b72428443856bbe1a9514
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117609610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b99a4410533bffa6b459825047f617013f9cca710fa4516833f49f1c8e99e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:46:54 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:55 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:46:56 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:57 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:46:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:46:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:35 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:37 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:39 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:40 GMT
CMD ["mysqld"]
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
	-	`sha256:1fe50c036dbc11c01a34966025f1bb13dd02d17d49adce519aa5f3476d6f657d`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3c32c10438dfc9e0ea677fad181e7f0003c745ce68a04bd9f99ca05b7fafb`  
		Last Modified: Fri, 07 Jan 2022 03:52:53 GMT  
		Size: 79.5 MB (79532877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb100408fe5bc48ae21ee3eb03b41c512b9a0112a935f76314a4bf6822f6c5`  
		Last Modified: Fri, 07 Jan 2022 03:52:41 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bc94fe194e8f25c01a2a754e78f55973c1b2b29263125ebe8538857a50a98`  
		Last Modified: Fri, 07 Jan 2022 03:52:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21c85126c6b1b052f6ece4aa553a8cb30b9d73a547817050e21c86c89884f962
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130990969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe75bce261a08b18e6c368d43a5edaa8a707c403a0f53d3ab2d7096c8eff081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:35 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:38 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 07 Jan 2022 03:45:42 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:44 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Fri, 07 Jan 2022 03:45:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:47:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:47:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:47:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:47:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:47:30 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:47:32 GMT
CMD ["mysqld"]
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
	-	`sha256:57c6fb78f11a792ad4c8b574f558f217d851c20fa967abf9ed942f00d1b44b66`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711fab5733e2c461a3619c5bf7850b929437cad2936cb023c30815a8dc5a9063`  
		Last Modified: Fri, 07 Jan 2022 03:55:57 GMT  
		Size: 84.8 MB (84784281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4225a61411885ccd66a7492ccdb59fcf5c039ee164cd0d2a4d10f2a1272bd0`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ab642f18817f4ea955bfcf14e679732ab440b7bc84be54b1149ed91bfff98b`  
		Last Modified: Fri, 07 Jan 2022 03:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:821d0411208eaa88f9e1f0daccd1d534f88d19baf724eb9a2777cbedb10b6c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:7f67b523cb7abb428055d8de0ef2b8e3da061b8ca37ce79c9f00132f915e3633
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124833490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39585239be1b14896801752f67d3bd7498488f441851bd7250fd773a741388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:32:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:56 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:57 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:57 GMT
CMD ["mysqld"]
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
	-	`sha256:1818b6d6a49996731a9c521becf0cf2f3b7f3ed67d1f821df22eac5a0a828e55`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d0ceb25218c827579a5da01c4924f7ee1d862cb3839156f0462a4da6aeb010`  
		Last Modified: Fri, 07 Jan 2022 03:37:17 GMT  
		Size: 84.9 MB (84909336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f75acc34fd9124f31fd89ac18cd948e4719d37eaa2a861bc58d6cfc168dc`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b01125470d6615164ad68a429b84831252908ec8ce316f3f9c6a7042039`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e9be9a54da1f573f75e63153a51a68b4897c4e55d14260b8c3c20151e7160bb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122256926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc8711797847fd73d0a82346de2db687832d0cd05caec061e7a0125def465ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:53 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:55 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:56 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:46:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:46:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:46:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:46:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:46:42 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:46:43 GMT
CMD ["mysqld"]
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
	-	`sha256:57c9ab136e49c3631482d96d7165a4a35534cc02050a9799764882822f15769b`  
		Last Modified: Fri, 07 Jan 2022 03:52:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbff49208522033a770abada0026d29fea689fd3a3c984e6fd884f6308a7fdb8`  
		Last Modified: Fri, 07 Jan 2022 03:52:21 GMT  
		Size: 84.2 MB (84180193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c0a598b42f85dd5fd378a607faf0ee8b2765f79643c5213407e4144239d5`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a241bbd5a0cfbf551426d3ee2bb62488a8c5399d1e3e1fc2f264f0c653a9f2`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:807b1f8ddba41d7f2b33d5a85ca0b49b1fb0025b0210edce5f9cc0f47b51fcc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135597698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a198ad3e6cf366e01dbaba4adbb38c88658af88a7981e16d3a2eb27b7e1c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:43:26 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:28 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:31 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:45:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:26 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:28 GMT
CMD ["mysqld"]
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
	-	`sha256:37b482633cfa67a2c551773a43b65a9cd6d59f33d58ae835b62e65930512de4c`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0e90247ffcbc43167e2c35ca07822c0cae59b6e3449d7235594361a8640e8`  
		Last Modified: Fri, 07 Jan 2022 03:55:18 GMT  
		Size: 89.4 MB (89391008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611041c6b3fc07063403a3af6ce1a23364e52f378718357b228c37136499eee`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e14164bc7a8b6f42ad36bc59c5be9819d8b00792d59a5d48d1452ee33f8890`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:821d0411208eaa88f9e1f0daccd1d534f88d19baf724eb9a2777cbedb10b6c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7f67b523cb7abb428055d8de0ef2b8e3da061b8ca37ce79c9f00132f915e3633
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124833490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39585239be1b14896801752f67d3bd7498488f441851bd7250fd773a741388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:32:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:56 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:57 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:57 GMT
CMD ["mysqld"]
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
	-	`sha256:1818b6d6a49996731a9c521becf0cf2f3b7f3ed67d1f821df22eac5a0a828e55`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d0ceb25218c827579a5da01c4924f7ee1d862cb3839156f0462a4da6aeb010`  
		Last Modified: Fri, 07 Jan 2022 03:37:17 GMT  
		Size: 84.9 MB (84909336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f75acc34fd9124f31fd89ac18cd948e4719d37eaa2a861bc58d6cfc168dc`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b01125470d6615164ad68a429b84831252908ec8ce316f3f9c6a7042039`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e9be9a54da1f573f75e63153a51a68b4897c4e55d14260b8c3c20151e7160bb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122256926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc8711797847fd73d0a82346de2db687832d0cd05caec061e7a0125def465ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:53 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:55 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:56 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:46:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:46:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:46:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:46:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:46:42 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:46:43 GMT
CMD ["mysqld"]
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
	-	`sha256:57c9ab136e49c3631482d96d7165a4a35534cc02050a9799764882822f15769b`  
		Last Modified: Fri, 07 Jan 2022 03:52:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbff49208522033a770abada0026d29fea689fd3a3c984e6fd884f6308a7fdb8`  
		Last Modified: Fri, 07 Jan 2022 03:52:21 GMT  
		Size: 84.2 MB (84180193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c0a598b42f85dd5fd378a607faf0ee8b2765f79643c5213407e4144239d5`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a241bbd5a0cfbf551426d3ee2bb62488a8c5399d1e3e1fc2f264f0c653a9f2`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:807b1f8ddba41d7f2b33d5a85ca0b49b1fb0025b0210edce5f9cc0f47b51fcc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135597698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a198ad3e6cf366e01dbaba4adbb38c88658af88a7981e16d3a2eb27b7e1c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:43:26 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:28 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:31 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:45:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:26 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:28 GMT
CMD ["mysqld"]
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
	-	`sha256:37b482633cfa67a2c551773a43b65a9cd6d59f33d58ae835b62e65930512de4c`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0e90247ffcbc43167e2c35ca07822c0cae59b6e3449d7235594361a8640e8`  
		Last Modified: Fri, 07 Jan 2022 03:55:18 GMT  
		Size: 89.4 MB (89391008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611041c6b3fc07063403a3af6ce1a23364e52f378718357b228c37136499eee`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e14164bc7a8b6f42ad36bc59c5be9819d8b00792d59a5d48d1452ee33f8890`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22`

```console
$ docker pull mariadb@sha256:821d0411208eaa88f9e1f0daccd1d534f88d19baf724eb9a2777cbedb10b6c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22` - linux; amd64

```console
$ docker pull mariadb@sha256:7f67b523cb7abb428055d8de0ef2b8e3da061b8ca37ce79c9f00132f915e3633
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124833490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39585239be1b14896801752f67d3bd7498488f441851bd7250fd773a741388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:32:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:56 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:57 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:57 GMT
CMD ["mysqld"]
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
	-	`sha256:1818b6d6a49996731a9c521becf0cf2f3b7f3ed67d1f821df22eac5a0a828e55`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d0ceb25218c827579a5da01c4924f7ee1d862cb3839156f0462a4da6aeb010`  
		Last Modified: Fri, 07 Jan 2022 03:37:17 GMT  
		Size: 84.9 MB (84909336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f75acc34fd9124f31fd89ac18cd948e4719d37eaa2a861bc58d6cfc168dc`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b01125470d6615164ad68a429b84831252908ec8ce316f3f9c6a7042039`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e9be9a54da1f573f75e63153a51a68b4897c4e55d14260b8c3c20151e7160bb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122256926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc8711797847fd73d0a82346de2db687832d0cd05caec061e7a0125def465ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:53 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:55 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:56 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:46:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:46:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:46:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:46:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:46:42 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:46:43 GMT
CMD ["mysqld"]
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
	-	`sha256:57c9ab136e49c3631482d96d7165a4a35534cc02050a9799764882822f15769b`  
		Last Modified: Fri, 07 Jan 2022 03:52:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbff49208522033a770abada0026d29fea689fd3a3c984e6fd884f6308a7fdb8`  
		Last Modified: Fri, 07 Jan 2022 03:52:21 GMT  
		Size: 84.2 MB (84180193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c0a598b42f85dd5fd378a607faf0ee8b2765f79643c5213407e4144239d5`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a241bbd5a0cfbf551426d3ee2bb62488a8c5399d1e3e1fc2f264f0c653a9f2`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; ppc64le

```console
$ docker pull mariadb@sha256:807b1f8ddba41d7f2b33d5a85ca0b49b1fb0025b0210edce5f9cc0f47b51fcc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135597698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a198ad3e6cf366e01dbaba4adbb38c88658af88a7981e16d3a2eb27b7e1c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:43:26 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:28 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:31 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:45:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:26 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:28 GMT
CMD ["mysqld"]
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
	-	`sha256:37b482633cfa67a2c551773a43b65a9cd6d59f33d58ae835b62e65930512de4c`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0e90247ffcbc43167e2c35ca07822c0cae59b6e3449d7235594361a8640e8`  
		Last Modified: Fri, 07 Jan 2022 03:55:18 GMT  
		Size: 89.4 MB (89391008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611041c6b3fc07063403a3af6ce1a23364e52f378718357b228c37136499eee`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e14164bc7a8b6f42ad36bc59c5be9819d8b00792d59a5d48d1452ee33f8890`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22-focal`

```console
$ docker pull mariadb@sha256:821d0411208eaa88f9e1f0daccd1d534f88d19baf724eb9a2777cbedb10b6c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7f67b523cb7abb428055d8de0ef2b8e3da061b8ca37ce79c9f00132f915e3633
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124833490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f39585239be1b14896801752f67d3bd7498488f441851bd7250fd773a741388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:32:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:32:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:32:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:56 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:57 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:57 GMT
CMD ["mysqld"]
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
	-	`sha256:1818b6d6a49996731a9c521becf0cf2f3b7f3ed67d1f821df22eac5a0a828e55`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d0ceb25218c827579a5da01c4924f7ee1d862cb3839156f0462a4da6aeb010`  
		Last Modified: Fri, 07 Jan 2022 03:37:17 GMT  
		Size: 84.9 MB (84909336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f75acc34fd9124f31fd89ac18cd948e4719d37eaa2a861bc58d6cfc168dc`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b01125470d6615164ad68a429b84831252908ec8ce316f3f9c6a7042039`  
		Last Modified: Fri, 07 Jan 2022 03:37:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e9be9a54da1f573f75e63153a51a68b4897c4e55d14260b8c3c20151e7160bb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122256926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc8711797847fd73d0a82346de2db687832d0cd05caec061e7a0125def465ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:53 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:45:55 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:56 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:45:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:46:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:46:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:46:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:46:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:46:42 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:46:43 GMT
CMD ["mysqld"]
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
	-	`sha256:57c9ab136e49c3631482d96d7165a4a35534cc02050a9799764882822f15769b`  
		Last Modified: Fri, 07 Jan 2022 03:52:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbff49208522033a770abada0026d29fea689fd3a3c984e6fd884f6308a7fdb8`  
		Last Modified: Fri, 07 Jan 2022 03:52:21 GMT  
		Size: 84.2 MB (84180193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a348c0a598b42f85dd5fd378a607faf0ee8b2765f79643c5213407e4144239d5`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a241bbd5a0cfbf551426d3ee2bb62488a8c5399d1e3e1fc2f264f0c653a9f2`  
		Last Modified: Fri, 07 Jan 2022 03:52:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:807b1f8ddba41d7f2b33d5a85ca0b49b1fb0025b0210edce5f9cc0f47b51fcc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135597698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a198ad3e6cf366e01dbaba4adbb38c88658af88a7981e16d3a2eb27b7e1c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:43:26 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:28 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 07 Jan 2022 03:43:30 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:31 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Fri, 07 Jan 2022 03:43:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 07 Jan 2022 03:45:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:26 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:28 GMT
CMD ["mysqld"]
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
	-	`sha256:37b482633cfa67a2c551773a43b65a9cd6d59f33d58ae835b62e65930512de4c`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0e90247ffcbc43167e2c35ca07822c0cae59b6e3449d7235594361a8640e8`  
		Last Modified: Fri, 07 Jan 2022 03:55:18 GMT  
		Size: 89.4 MB (89391008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611041c6b3fc07063403a3af6ce1a23364e52f378718357b228c37136499eee`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e14164bc7a8b6f42ad36bc59c5be9819d8b00792d59a5d48d1452ee33f8890`  
		Last Modified: Fri, 07 Jan 2022 03:55:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:4766f321f60d25c07e7ea5cedc9251ccb7a464f86801a198926cc642e038303d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:1bab6b6537eea75ba33e431b000c82d33bec61f68c9ed9baec3b058baf73fdaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db72891d344da0a869b3ea44630259c8a9b1aefbbd8358905d7bfc04c34fc9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:31:56 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:31:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:22 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:22 GMT
CMD ["mysqld"]
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
	-	`sha256:1e8a0963e20973f8e2d92d2aead686937f537e283dc35f8a932e58b67a007aa9`  
		Last Modified: Fri, 07 Jan 2022 03:36:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b9584267073b1d8ef71579d35e756af3a7a15df656104f563ae23371d3c6c`  
		Last Modified: Fri, 07 Jan 2022 03:36:48 GMT  
		Size: 87.1 MB (87091366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e49646348722d85ef10e92011174cbda94484bd9ecb4cfec9c5a1be1a5bee5`  
		Last Modified: Fri, 07 Jan 2022 03:36:35 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dfec16a438568c09853d160dd848a3baa5a0bce3ea0c112ffa88168c47ba7f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124287071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475bc80a850a4c120dc91936174a27d0416ade2b04f5553f7cdbc0a5642cf19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:08 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:09 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:10 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:11 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:46 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:47 GMT
CMD ["mysqld"]
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
	-	`sha256:0c26aca3b84202eb22c8635874e7001f4c5654cbfaaf0aa775735a14342a7d3e`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0338485b57183f44125d85fd10c06189155deabea23805051d312c4e01aed392`  
		Last Modified: Fri, 07 Jan 2022 03:51:50 GMT  
		Size: 86.2 MB (86210460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec908cf7c03c27310d10e9eb5f5335c414b4edd769d0abec549e139259014b5`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:234be8c4f4ec9beb0484712c04e9490565ee4e618adf2b89942e8ce60d5380e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137741820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d75572a30f042be859485567b60045b073140bb6e1b38faeb077da81980d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:41:15 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:18 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:20 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:22 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:41:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:43:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:43:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:43:12 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:43:15 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:43:18 GMT
CMD ["mysqld"]
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
	-	`sha256:051e341941ad6bcccd5e3ee14814afec2339bf4bc5f7c00ff0e1e2ce2040b05b`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280462db5ca1e18f359c79ce539e1e6266d1fadf4099ca70b4bb927f0746bcc8`  
		Last Modified: Fri, 07 Jan 2022 03:54:40 GMT  
		Size: 91.5 MB (91535255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61693cce46aa3c168e64e107129225e003b9b9ae403444c05b75f2cfc5c70388`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:b1afc0429cba9ebc5e33976f60da5042d77ae17ba7a71a162538dd6a3864475a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126209287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd68c751f9352d2a8b9072846ce5c74dd359f37ca62d0139355d2db2db36a80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:37:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:37:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:38:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:38:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:38:02 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:38:02 GMT
CMD ["mysqld"]
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
	-	`sha256:5194d1aae7317f15c1bb03648a96b196033071aeb17dbd609225d6edf47edae8`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3981fc26ffd142d6b7a8732e8a236adb479da75c8692ccb9ed6ddd45198c5`  
		Last Modified: Fri, 07 Jan 2022 02:39:56 GMT  
		Size: 88.3 MB (88266598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac1fc82c1dc6889f8b3a05a1bf89ecb6ce97fe4258c9b50ed1c63811c9db6`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:4766f321f60d25c07e7ea5cedc9251ccb7a464f86801a198926cc642e038303d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1bab6b6537eea75ba33e431b000c82d33bec61f68c9ed9baec3b058baf73fdaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db72891d344da0a869b3ea44630259c8a9b1aefbbd8358905d7bfc04c34fc9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:31:56 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:31:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:22 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:22 GMT
CMD ["mysqld"]
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
	-	`sha256:1e8a0963e20973f8e2d92d2aead686937f537e283dc35f8a932e58b67a007aa9`  
		Last Modified: Fri, 07 Jan 2022 03:36:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b9584267073b1d8ef71579d35e756af3a7a15df656104f563ae23371d3c6c`  
		Last Modified: Fri, 07 Jan 2022 03:36:48 GMT  
		Size: 87.1 MB (87091366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e49646348722d85ef10e92011174cbda94484bd9ecb4cfec9c5a1be1a5bee5`  
		Last Modified: Fri, 07 Jan 2022 03:36:35 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dfec16a438568c09853d160dd848a3baa5a0bce3ea0c112ffa88168c47ba7f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124287071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475bc80a850a4c120dc91936174a27d0416ade2b04f5553f7cdbc0a5642cf19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:08 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:09 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:10 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:11 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:46 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:47 GMT
CMD ["mysqld"]
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
	-	`sha256:0c26aca3b84202eb22c8635874e7001f4c5654cbfaaf0aa775735a14342a7d3e`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0338485b57183f44125d85fd10c06189155deabea23805051d312c4e01aed392`  
		Last Modified: Fri, 07 Jan 2022 03:51:50 GMT  
		Size: 86.2 MB (86210460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec908cf7c03c27310d10e9eb5f5335c414b4edd769d0abec549e139259014b5`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:234be8c4f4ec9beb0484712c04e9490565ee4e618adf2b89942e8ce60d5380e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137741820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d75572a30f042be859485567b60045b073140bb6e1b38faeb077da81980d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:41:15 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:18 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:20 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:22 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:41:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:43:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:43:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:43:12 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:43:15 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:43:18 GMT
CMD ["mysqld"]
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
	-	`sha256:051e341941ad6bcccd5e3ee14814afec2339bf4bc5f7c00ff0e1e2ce2040b05b`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280462db5ca1e18f359c79ce539e1e6266d1fadf4099ca70b4bb927f0746bcc8`  
		Last Modified: Fri, 07 Jan 2022 03:54:40 GMT  
		Size: 91.5 MB (91535255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61693cce46aa3c168e64e107129225e003b9b9ae403444c05b75f2cfc5c70388`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b1afc0429cba9ebc5e33976f60da5042d77ae17ba7a71a162538dd6a3864475a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126209287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd68c751f9352d2a8b9072846ce5c74dd359f37ca62d0139355d2db2db36a80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:37:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:37:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:38:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:38:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:38:02 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:38:02 GMT
CMD ["mysqld"]
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
	-	`sha256:5194d1aae7317f15c1bb03648a96b196033071aeb17dbd609225d6edf47edae8`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3981fc26ffd142d6b7a8732e8a236adb479da75c8692ccb9ed6ddd45198c5`  
		Last Modified: Fri, 07 Jan 2022 02:39:56 GMT  
		Size: 88.3 MB (88266598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac1fc82c1dc6889f8b3a05a1bf89ecb6ce97fe4258c9b50ed1c63811c9db6`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.13`

```console
$ docker pull mariadb@sha256:4766f321f60d25c07e7ea5cedc9251ccb7a464f86801a198926cc642e038303d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13` - linux; amd64

```console
$ docker pull mariadb@sha256:1bab6b6537eea75ba33e431b000c82d33bec61f68c9ed9baec3b058baf73fdaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db72891d344da0a869b3ea44630259c8a9b1aefbbd8358905d7bfc04c34fc9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:31:56 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:31:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:22 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:22 GMT
CMD ["mysqld"]
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
	-	`sha256:1e8a0963e20973f8e2d92d2aead686937f537e283dc35f8a932e58b67a007aa9`  
		Last Modified: Fri, 07 Jan 2022 03:36:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b9584267073b1d8ef71579d35e756af3a7a15df656104f563ae23371d3c6c`  
		Last Modified: Fri, 07 Jan 2022 03:36:48 GMT  
		Size: 87.1 MB (87091366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e49646348722d85ef10e92011174cbda94484bd9ecb4cfec9c5a1be1a5bee5`  
		Last Modified: Fri, 07 Jan 2022 03:36:35 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dfec16a438568c09853d160dd848a3baa5a0bce3ea0c112ffa88168c47ba7f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124287071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475bc80a850a4c120dc91936174a27d0416ade2b04f5553f7cdbc0a5642cf19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:08 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:09 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:10 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:11 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:46 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:47 GMT
CMD ["mysqld"]
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
	-	`sha256:0c26aca3b84202eb22c8635874e7001f4c5654cbfaaf0aa775735a14342a7d3e`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0338485b57183f44125d85fd10c06189155deabea23805051d312c4e01aed392`  
		Last Modified: Fri, 07 Jan 2022 03:51:50 GMT  
		Size: 86.2 MB (86210460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec908cf7c03c27310d10e9eb5f5335c414b4edd769d0abec549e139259014b5`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:234be8c4f4ec9beb0484712c04e9490565ee4e618adf2b89942e8ce60d5380e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137741820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d75572a30f042be859485567b60045b073140bb6e1b38faeb077da81980d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:41:15 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:18 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:20 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:22 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:41:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:43:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:43:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:43:12 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:43:15 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:43:18 GMT
CMD ["mysqld"]
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
	-	`sha256:051e341941ad6bcccd5e3ee14814afec2339bf4bc5f7c00ff0e1e2ce2040b05b`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280462db5ca1e18f359c79ce539e1e6266d1fadf4099ca70b4bb927f0746bcc8`  
		Last Modified: Fri, 07 Jan 2022 03:54:40 GMT  
		Size: 91.5 MB (91535255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61693cce46aa3c168e64e107129225e003b9b9ae403444c05b75f2cfc5c70388`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; s390x

```console
$ docker pull mariadb@sha256:b1afc0429cba9ebc5e33976f60da5042d77ae17ba7a71a162538dd6a3864475a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126209287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd68c751f9352d2a8b9072846ce5c74dd359f37ca62d0139355d2db2db36a80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:37:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:37:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:38:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:38:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:38:02 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:38:02 GMT
CMD ["mysqld"]
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
	-	`sha256:5194d1aae7317f15c1bb03648a96b196033071aeb17dbd609225d6edf47edae8`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3981fc26ffd142d6b7a8732e8a236adb479da75c8692ccb9ed6ddd45198c5`  
		Last Modified: Fri, 07 Jan 2022 02:39:56 GMT  
		Size: 88.3 MB (88266598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac1fc82c1dc6889f8b3a05a1bf89ecb6ce97fe4258c9b50ed1c63811c9db6`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.13-focal`

```console
$ docker pull mariadb@sha256:4766f321f60d25c07e7ea5cedc9251ccb7a464f86801a198926cc642e038303d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1bab6b6537eea75ba33e431b000c82d33bec61f68c9ed9baec3b058baf73fdaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db72891d344da0a869b3ea44630259c8a9b1aefbbd8358905d7bfc04c34fc9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:31:56 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:31:57 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:31:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:31:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:32:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:32:22 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:32:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:32:22 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:32:22 GMT
CMD ["mysqld"]
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
	-	`sha256:1e8a0963e20973f8e2d92d2aead686937f537e283dc35f8a932e58b67a007aa9`  
		Last Modified: Fri, 07 Jan 2022 03:36:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b9584267073b1d8ef71579d35e756af3a7a15df656104f563ae23371d3c6c`  
		Last Modified: Fri, 07 Jan 2022 03:36:48 GMT  
		Size: 87.1 MB (87091366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e49646348722d85ef10e92011174cbda94484bd9ecb4cfec9c5a1be1a5bee5`  
		Last Modified: Fri, 07 Jan 2022 03:36:35 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dfec16a438568c09853d160dd848a3baa5a0bce3ea0c112ffa88168c47ba7f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124287071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475bc80a850a4c120dc91936174a27d0416ade2b04f5553f7cdbc0a5642cf19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:45:08 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:09 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:45:10 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:11 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:45:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:45:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:45:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:45:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:45:46 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:45:47 GMT
CMD ["mysqld"]
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
	-	`sha256:0c26aca3b84202eb22c8635874e7001f4c5654cbfaaf0aa775735a14342a7d3e`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0338485b57183f44125d85fd10c06189155deabea23805051d312c4e01aed392`  
		Last Modified: Fri, 07 Jan 2022 03:51:50 GMT  
		Size: 86.2 MB (86210460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec908cf7c03c27310d10e9eb5f5335c414b4edd769d0abec549e139259014b5`  
		Last Modified: Fri, 07 Jan 2022 03:51:37 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:234be8c4f4ec9beb0484712c04e9490565ee4e618adf2b89942e8ce60d5380e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137741820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d75572a30f042be859485567b60045b073140bb6e1b38faeb077da81980d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 03:41:15 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:18 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 03:41:20 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:22 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 03:41:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:41:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:43:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:43:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:43:12 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:43:15 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:43:18 GMT
CMD ["mysqld"]
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
	-	`sha256:051e341941ad6bcccd5e3ee14814afec2339bf4bc5f7c00ff0e1e2ce2040b05b`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280462db5ca1e18f359c79ce539e1e6266d1fadf4099ca70b4bb927f0746bcc8`  
		Last Modified: Fri, 07 Jan 2022 03:54:40 GMT  
		Size: 91.5 MB (91535255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61693cce46aa3c168e64e107129225e003b9b9ae403444c05b75f2cfc5c70388`  
		Last Modified: Fri, 07 Jan 2022 03:54:22 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b1afc0429cba9ebc5e33976f60da5042d77ae17ba7a71a162538dd6a3864475a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126209287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd68c751f9352d2a8b9072846ce5c74dd359f37ca62d0139355d2db2db36a80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

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
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 07 Jan 2022 02:37:38 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Fri, 07 Jan 2022 02:37:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:37:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:37:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:38:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:38:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:38:02 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:38:02 GMT
CMD ["mysqld"]
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
	-	`sha256:5194d1aae7317f15c1bb03648a96b196033071aeb17dbd609225d6edf47edae8`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3981fc26ffd142d6b7a8732e8a236adb479da75c8692ccb9ed6ddd45198c5`  
		Last Modified: Fri, 07 Jan 2022 02:39:56 GMT  
		Size: 88.3 MB (88266598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac1fc82c1dc6889f8b3a05a1bf89ecb6ce97fe4258c9b50ed1c63811c9db6`  
		Last Modified: Fri, 07 Jan 2022 02:39:44 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

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

### `mariadb:10.6` - linux; arm64 variant v8

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

### `mariadb:10.6` - linux; ppc64le

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

### `mariadb:10.6` - linux; s390x

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

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

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

### `mariadb:10.6-focal` - linux; arm64 variant v8

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

### `mariadb:10.6-focal` - linux; ppc64le

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

### `mariadb:10.6-focal` - linux; s390x

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

## `mariadb:10.6.5`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5` - linux; amd64

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

### `mariadb:10.6.5` - linux; arm64 variant v8

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

### `mariadb:10.6.5` - linux; ppc64le

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

### `mariadb:10.6.5` - linux; s390x

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

## `mariadb:10.6.5-focal`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5-focal` - linux; amd64

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

### `mariadb:10.6.5-focal` - linux; arm64 variant v8

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

### `mariadb:10.6.5-focal` - linux; ppc64le

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

### `mariadb:10.6.5-focal` - linux; s390x

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

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:a469ba5edc9267eb3f32f5a6773376677274b09d36bbe742b448fc4c787e6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:e2480ebe67bf4e76f063e7ec96e721fb9f8ac1b9400c5e3fde296215d7aa4fba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127712884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e98561d2cc9b03f8bd50f9824ab2a1d13502d2fa39456e0eb8e3dc5f29f597`
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
# Fri, 07 Jan 2022 03:30:40 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:40 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:41 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:31:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:31:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:31:17 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:31:17 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:31:17 GMT
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
	-	`sha256:2377119eafec5b3575888ca5ff24c8c26af900dda0f56089bf053fcca0ca6517`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d493bc9f2ca03d3fcfbc2dc9c51783bd2298937284de547af92526f5e9639c`  
		Last Modified: Fri, 07 Jan 2022 03:35:41 GMT  
		Size: 87.8 MB (87788854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd0778bc1e1506cea66ec6a5777ceb5e4f2bfa498f6aa671b0665f970f4e0a1`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ac59164358e9d70552fec41ca883912246d11aed8955e0a07fdcd44eacad24af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124869502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09d0628419715ae6cc81d4a3aa3bf4ee89515a2ba7c504d9fa9333114a0e57`
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
# Fri, 07 Jan 2022 03:43:22 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:24 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:25 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:44:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:44:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:44:03 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:44:04 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:44:05 GMT
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
	-	`sha256:38966b681400e819ec825e3f9bf579711f8ca22f0b705998358d6c7c45c051a3`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff7d8177c17a7fbd90975e812b80f728d163e6c253e198ca0a4cd476ff4a86`  
		Last Modified: Fri, 07 Jan 2022 03:50:34 GMT  
		Size: 86.8 MB (86792893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f79b6bc04c49c43f894d979790fc17809940b9f161380a21b71de12513183`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0287e0b63ad95b096164b847e985a08451f458a54998659fb3adc21323214eaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cdbfc67ec3d7bbeb6e2b5862eedf286a9d1a71f492856418c633c553bb3b48`
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
# Fri, 07 Jan 2022 03:36:45 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:48 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:50 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:52 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:36:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:38:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:38:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:38:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:38:48 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:38:51 GMT
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
	-	`sha256:2f46878b387824c89ae8398faa258e660a18526224791a0242a33c37271e35a3`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02409bdc6f658420bfaff21be4e0c97fe8eb00366911d44bbafec02d5243f57`  
		Last Modified: Fri, 07 Jan 2022 03:53:11 GMT  
		Size: 92.2 MB (92226663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3c1ce23a9cc25188bdb9de4ff87f8b2bc482d4f0586326c916092a6b9acd8`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:5dd0a1ebeb07f851ea5ac4109809e733aab37c8a44533aa2e0ed554c3cc3226a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126702080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e5a237e06081108447dab567d5a2dc3c83a8fad5cb08c4cd28852e24db132`
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
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:36:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:36:40 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:36:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:36:41 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:36:41 GMT
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
	-	`sha256:d348b4a093788d619d93351ae86741ab65a67d3d48ce1bff2f8b43682b271509`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908f3b022085417ffa7577f0931e76f4c2fca5d8780bd41b70c2d65ab3cf075b`  
		Last Modified: Fri, 07 Jan 2022 02:38:58 GMT  
		Size: 88.8 MB (88759391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402de412f628fdc4ba59938703f8d823f15665d59b9ab1c8542cb9d93e53e1ea`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:a469ba5edc9267eb3f32f5a6773376677274b09d36bbe742b448fc4c787e6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:e2480ebe67bf4e76f063e7ec96e721fb9f8ac1b9400c5e3fde296215d7aa4fba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127712884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e98561d2cc9b03f8bd50f9824ab2a1d13502d2fa39456e0eb8e3dc5f29f597`
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
# Fri, 07 Jan 2022 03:30:40 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:40 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:41 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:31:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:31:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:31:17 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:31:17 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:31:17 GMT
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
	-	`sha256:2377119eafec5b3575888ca5ff24c8c26af900dda0f56089bf053fcca0ca6517`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d493bc9f2ca03d3fcfbc2dc9c51783bd2298937284de547af92526f5e9639c`  
		Last Modified: Fri, 07 Jan 2022 03:35:41 GMT  
		Size: 87.8 MB (87788854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd0778bc1e1506cea66ec6a5777ceb5e4f2bfa498f6aa671b0665f970f4e0a1`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ac59164358e9d70552fec41ca883912246d11aed8955e0a07fdcd44eacad24af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124869502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09d0628419715ae6cc81d4a3aa3bf4ee89515a2ba7c504d9fa9333114a0e57`
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
# Fri, 07 Jan 2022 03:43:22 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:24 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:25 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:44:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:44:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:44:03 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:44:04 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:44:05 GMT
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
	-	`sha256:38966b681400e819ec825e3f9bf579711f8ca22f0b705998358d6c7c45c051a3`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff7d8177c17a7fbd90975e812b80f728d163e6c253e198ca0a4cd476ff4a86`  
		Last Modified: Fri, 07 Jan 2022 03:50:34 GMT  
		Size: 86.8 MB (86792893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f79b6bc04c49c43f894d979790fc17809940b9f161380a21b71de12513183`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0287e0b63ad95b096164b847e985a08451f458a54998659fb3adc21323214eaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cdbfc67ec3d7bbeb6e2b5862eedf286a9d1a71f492856418c633c553bb3b48`
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
# Fri, 07 Jan 2022 03:36:45 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:48 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:50 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:52 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:36:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:38:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:38:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:38:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:38:48 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:38:51 GMT
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
	-	`sha256:2f46878b387824c89ae8398faa258e660a18526224791a0242a33c37271e35a3`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02409bdc6f658420bfaff21be4e0c97fe8eb00366911d44bbafec02d5243f57`  
		Last Modified: Fri, 07 Jan 2022 03:53:11 GMT  
		Size: 92.2 MB (92226663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3c1ce23a9cc25188bdb9de4ff87f8b2bc482d4f0586326c916092a6b9acd8`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:5dd0a1ebeb07f851ea5ac4109809e733aab37c8a44533aa2e0ed554c3cc3226a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126702080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e5a237e06081108447dab567d5a2dc3c83a8fad5cb08c4cd28852e24db132`
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
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:36:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:36:40 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:36:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:36:41 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:36:41 GMT
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
	-	`sha256:d348b4a093788d619d93351ae86741ab65a67d3d48ce1bff2f8b43682b271509`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908f3b022085417ffa7577f0931e76f4c2fca5d8780bd41b70c2d65ab3cf075b`  
		Last Modified: Fri, 07 Jan 2022 02:38:58 GMT  
		Size: 88.8 MB (88759391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402de412f628fdc4ba59938703f8d823f15665d59b9ab1c8542cb9d93e53e1ea`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.1`

```console
$ docker pull mariadb@sha256:a469ba5edc9267eb3f32f5a6773376677274b09d36bbe742b448fc4c787e6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1` - linux; amd64

```console
$ docker pull mariadb@sha256:e2480ebe67bf4e76f063e7ec96e721fb9f8ac1b9400c5e3fde296215d7aa4fba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127712884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e98561d2cc9b03f8bd50f9824ab2a1d13502d2fa39456e0eb8e3dc5f29f597`
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
# Fri, 07 Jan 2022 03:30:40 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:40 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:41 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:31:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:31:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:31:17 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:31:17 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:31:17 GMT
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
	-	`sha256:2377119eafec5b3575888ca5ff24c8c26af900dda0f56089bf053fcca0ca6517`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d493bc9f2ca03d3fcfbc2dc9c51783bd2298937284de547af92526f5e9639c`  
		Last Modified: Fri, 07 Jan 2022 03:35:41 GMT  
		Size: 87.8 MB (87788854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd0778bc1e1506cea66ec6a5777ceb5e4f2bfa498f6aa671b0665f970f4e0a1`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ac59164358e9d70552fec41ca883912246d11aed8955e0a07fdcd44eacad24af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124869502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09d0628419715ae6cc81d4a3aa3bf4ee89515a2ba7c504d9fa9333114a0e57`
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
# Fri, 07 Jan 2022 03:43:22 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:24 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:25 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:44:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:44:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:44:03 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:44:04 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:44:05 GMT
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
	-	`sha256:38966b681400e819ec825e3f9bf579711f8ca22f0b705998358d6c7c45c051a3`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff7d8177c17a7fbd90975e812b80f728d163e6c253e198ca0a4cd476ff4a86`  
		Last Modified: Fri, 07 Jan 2022 03:50:34 GMT  
		Size: 86.8 MB (86792893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f79b6bc04c49c43f894d979790fc17809940b9f161380a21b71de12513183`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0287e0b63ad95b096164b847e985a08451f458a54998659fb3adc21323214eaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cdbfc67ec3d7bbeb6e2b5862eedf286a9d1a71f492856418c633c553bb3b48`
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
# Fri, 07 Jan 2022 03:36:45 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:48 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:50 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:52 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:36:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:38:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:38:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:38:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:38:48 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:38:51 GMT
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
	-	`sha256:2f46878b387824c89ae8398faa258e660a18526224791a0242a33c37271e35a3`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02409bdc6f658420bfaff21be4e0c97fe8eb00366911d44bbafec02d5243f57`  
		Last Modified: Fri, 07 Jan 2022 03:53:11 GMT  
		Size: 92.2 MB (92226663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3c1ce23a9cc25188bdb9de4ff87f8b2bc482d4f0586326c916092a6b9acd8`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; s390x

```console
$ docker pull mariadb@sha256:5dd0a1ebeb07f851ea5ac4109809e733aab37c8a44533aa2e0ed554c3cc3226a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126702080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e5a237e06081108447dab567d5a2dc3c83a8fad5cb08c4cd28852e24db132`
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
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:36:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:36:40 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:36:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:36:41 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:36:41 GMT
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
	-	`sha256:d348b4a093788d619d93351ae86741ab65a67d3d48ce1bff2f8b43682b271509`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908f3b022085417ffa7577f0931e76f4c2fca5d8780bd41b70c2d65ab3cf075b`  
		Last Modified: Fri, 07 Jan 2022 02:38:58 GMT  
		Size: 88.8 MB (88759391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402de412f628fdc4ba59938703f8d823f15665d59b9ab1c8542cb9d93e53e1ea`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.1-focal`

```console
$ docker pull mariadb@sha256:a469ba5edc9267eb3f32f5a6773376677274b09d36bbe742b448fc4c787e6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:e2480ebe67bf4e76f063e7ec96e721fb9f8ac1b9400c5e3fde296215d7aa4fba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127712884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e98561d2cc9b03f8bd50f9824ab2a1d13502d2fa39456e0eb8e3dc5f29f597`
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
# Fri, 07 Jan 2022 03:30:40 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:40 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:30:41 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:31:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:31:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:31:17 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:31:17 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:31:17 GMT
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
	-	`sha256:2377119eafec5b3575888ca5ff24c8c26af900dda0f56089bf053fcca0ca6517`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d493bc9f2ca03d3fcfbc2dc9c51783bd2298937284de547af92526f5e9639c`  
		Last Modified: Fri, 07 Jan 2022 03:35:41 GMT  
		Size: 87.8 MB (87788854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd0778bc1e1506cea66ec6a5777ceb5e4f2bfa498f6aa671b0665f970f4e0a1`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ac59164358e9d70552fec41ca883912246d11aed8955e0a07fdcd44eacad24af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124869502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09d0628419715ae6cc81d4a3aa3bf4ee89515a2ba7c504d9fa9333114a0e57`
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
# Fri, 07 Jan 2022 03:43:22 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:43:24 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:25 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:43:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:44:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:44:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:44:03 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:44:04 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:44:05 GMT
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
	-	`sha256:38966b681400e819ec825e3f9bf579711f8ca22f0b705998358d6c7c45c051a3`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff7d8177c17a7fbd90975e812b80f728d163e6c253e198ca0a4cd476ff4a86`  
		Last Modified: Fri, 07 Jan 2022 03:50:34 GMT  
		Size: 86.8 MB (86792893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f79b6bc04c49c43f894d979790fc17809940b9f161380a21b71de12513183`  
		Last Modified: Fri, 07 Jan 2022 03:50:21 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0287e0b63ad95b096164b847e985a08451f458a54998659fb3adc21323214eaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cdbfc67ec3d7bbeb6e2b5862eedf286a9d1a71f492856418c633c553bb3b48`
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
# Fri, 07 Jan 2022 03:36:45 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:48 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 03:36:50 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:52 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 03:36:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 03:36:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 03:38:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 03:38:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 03:38:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:38:48 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 03:38:51 GMT
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
	-	`sha256:2f46878b387824c89ae8398faa258e660a18526224791a0242a33c37271e35a3`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02409bdc6f658420bfaff21be4e0c97fe8eb00366911d44bbafec02d5243f57`  
		Last Modified: Fri, 07 Jan 2022 03:53:11 GMT  
		Size: 92.2 MB (92226663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3c1ce23a9cc25188bdb9de4ff87f8b2bc482d4f0586326c916092a6b9acd8`  
		Last Modified: Fri, 07 Jan 2022 03:52:52 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:5dd0a1ebeb07f851ea5ac4109809e733aab37c8a44533aa2e0ed554c3cc3226a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126702080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e5a237e06081108447dab567d5a2dc3c83a8fad5cb08c4cd28852e24db132`
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
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 07 Jan 2022 02:36:16 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Fri, 07 Jan 2022 02:36:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Fri, 07 Jan 2022 02:36:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 07 Jan 2022 02:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 07 Jan 2022 02:36:40 GMT
VOLUME [/var/lib/mysql]
# Fri, 07 Jan 2022 02:36:40 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:36:41 GMT
EXPOSE 3306
# Fri, 07 Jan 2022 02:36:41 GMT
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
	-	`sha256:d348b4a093788d619d93351ae86741ab65a67d3d48ce1bff2f8b43682b271509`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908f3b022085417ffa7577f0931e76f4c2fca5d8780bd41b70c2d65ab3cf075b`  
		Last Modified: Fri, 07 Jan 2022 02:38:58 GMT  
		Size: 88.8 MB (88759391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402de412f628fdc4ba59938703f8d823f15665d59b9ab1c8542cb9d93e53e1ea`  
		Last Modified: Fri, 07 Jan 2022 02:38:45 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:5a37e65a6414d78f60d523c4ddcf93d715854337beb46f8beeb1a23d83262184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

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

### `mariadb:focal` - linux; arm64 variant v8

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

### `mariadb:focal` - linux; ppc64le

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

### `mariadb:focal` - linux; s390x

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
