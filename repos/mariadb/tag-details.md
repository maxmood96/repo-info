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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:3a4ab2d232d68eda6c02ac21b3d0117ba6826422095ffa19c7cc2947833dc3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:9f3d32d94acf1575778352a57736b8658b2e82914c95132e17cbae972ddd75d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109366470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da013e07658f467ba302052e465953694726c99953a0dc9a156a5607a984174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:14 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:32:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:32:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:32:49 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:32:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 01:33:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:33:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:33:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:33:43 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:33:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:33:44 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:33:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa82e4a480b0031196004180195fe405a9be3b3aa27b3a5707496385917e6f`  
		Last Modified: Wed, 10 Nov 2021 01:36:54 GMT  
		Size: 3.6 MB (3552876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8dfea7939d5fdf3afaf0e79ea3381ba8fa5be197d5e021c3cafb5444f7c90`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1650ff0f0b14f377b4cd4062abc5a68952d6cd4d96a445186049b6da8389f`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 1.6 MB (1583644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbbf5c0a7a156c68beab396f0f6a5c49f27d57afb630cab06111863ef3c0a04`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da10f864031144349b7bb74f484e2f733cf52c68f4346fb3dfe93438f4265c8e`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588fb2eae01fe7432714c5cd41cabc95d3e523000ae6788ee8900a98ad51eac`  
		Last Modified: Wed, 10 Nov 2021 01:37:01 GMT  
		Size: 72.7 MB (72698371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f7de3033fe99fc9691f6e3c6d70a829e5370bba6aa226a7701c2e826e9740c`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2edfd564b64d5f9d965e2380937a281db0aa8ff4e9152384de33a2c59cbc71`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:448a233b8d75def87d6db6cd6623a2042c1d9b97bba0d641a3f4988603a46d89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf901a92a5d2bc9cc1508a8d8a697d32b1fcf98a720b7473c710d5ca153ca69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:38 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Sat, 16 Oct 2021 01:47:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:48:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:49:08 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:51:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:52:06 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:52:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:52:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:52:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:52:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:52:22 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:24 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:25 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 00:52:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:52:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:52:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:53:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:53:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:53:03 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:53:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678889645a4645e6df6f5951b2faa756bcfc3a1c3a4d8b70126c8a381970e38`  
		Last Modified: Sat, 16 Oct 2021 03:53:30 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efc1be380cbc922ab4999aadde7b6c48c5228b757176209810d37554b2a056`  
		Last Modified: Sat, 16 Oct 2021 03:53:29 GMT  
		Size: 4.3 MB (4261579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d08baf1e962da42289483767cf16f450fa53b811b8ea12fcb586456118c231`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 3.2 MB (3207277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4740e2a70f5d2095f3d51954350c8e36372bfdf44b299200782ef6400531492`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d60a563e61658b2baa5c9a39817163d2495b9b95287924ce4df038e04064`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 1.5 MB (1529514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69340b12ab80abf3c9554baf7c743d8791a0d45fbbc9f2c7efefd4cfff119e`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5642e3f068c45be659c51cbca4d39a50fe31c60ec80358a64dc472e0eff1f5`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1cb90f79536f885082931f544d2493e28e994955deb5c3973f8efbcbe2e51`  
		Last Modified: Wed, 10 Nov 2021 00:57:05 GMT  
		Size: 71.5 MB (71495396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447a2046003f9b2338245d6ad83415cfac5530e4a9d96e874630928f08cb9cb`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d14c8dc2043c7306e2cac5e1e53f3dd2319ff5a5e5df8c5e116cc4daccabbe9`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aaa29bc3bab3a7aec9637991fbb009ab4524376f77d44750ec7601e3293f0c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117698933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83f8127b7c2500d881d29a5e4a43d45de6f693be38acf616e6b43d41bcdd4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:10:39 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 03:11:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 03:12:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 03:12:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:12:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 03:12:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:13:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:14 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:19 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 03:13:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:15:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:15:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:15:54 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:16:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:16:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:16:10 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:16:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d1b9e80c0330e70eec7e4746217b26e14d1a9e97a03bff51a6acf663a75a10`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 3.5 MB (3533213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927db937b773bb118edcd41e143a4b75710e7e45d1ebc181360edfa4a87818e7`  
		Last Modified: Wed, 10 Nov 2021 03:20:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3d24ccb97f9776893abffce060cc28690f9bafff16116a409e1bc224eb4356`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 1.9 MB (1937102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f83a0eeaf9b0378ef5be732c550cc019b529be4c9dad720f1aa6166b591e573`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9b0819ad891f7f8ac18418d3ddfb8265cd19728ed79ad2eb33e16e14a8136a`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e322340ec7651facf5e69b97fff295833396435f911081455778e986918f1`  
		Last Modified: Wed, 10 Nov 2021 03:21:10 GMT  
		Size: 76.2 MB (76152088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2d96724ea50492970d4833e3d6041f1c0999a3c8e38658a9ea49a0981eeb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d35b0dfeb42e74c605540f01f745397b7b8968ee399c173cd74c9726e68472`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:3a4ab2d232d68eda6c02ac21b3d0117ba6826422095ffa19c7cc2947833dc3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:9f3d32d94acf1575778352a57736b8658b2e82914c95132e17cbae972ddd75d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109366470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da013e07658f467ba302052e465953694726c99953a0dc9a156a5607a984174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:14 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:32:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:32:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:32:49 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:32:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 01:33:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:33:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:33:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:33:43 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:33:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:33:44 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:33:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa82e4a480b0031196004180195fe405a9be3b3aa27b3a5707496385917e6f`  
		Last Modified: Wed, 10 Nov 2021 01:36:54 GMT  
		Size: 3.6 MB (3552876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8dfea7939d5fdf3afaf0e79ea3381ba8fa5be197d5e021c3cafb5444f7c90`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1650ff0f0b14f377b4cd4062abc5a68952d6cd4d96a445186049b6da8389f`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 1.6 MB (1583644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbbf5c0a7a156c68beab396f0f6a5c49f27d57afb630cab06111863ef3c0a04`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da10f864031144349b7bb74f484e2f733cf52c68f4346fb3dfe93438f4265c8e`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588fb2eae01fe7432714c5cd41cabc95d3e523000ae6788ee8900a98ad51eac`  
		Last Modified: Wed, 10 Nov 2021 01:37:01 GMT  
		Size: 72.7 MB (72698371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f7de3033fe99fc9691f6e3c6d70a829e5370bba6aa226a7701c2e826e9740c`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2edfd564b64d5f9d965e2380937a281db0aa8ff4e9152384de33a2c59cbc71`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:448a233b8d75def87d6db6cd6623a2042c1d9b97bba0d641a3f4988603a46d89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf901a92a5d2bc9cc1508a8d8a697d32b1fcf98a720b7473c710d5ca153ca69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:38 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Sat, 16 Oct 2021 01:47:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:48:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:49:08 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:51:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:52:06 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:52:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:52:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:52:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:52:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:52:22 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:24 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:25 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 00:52:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:52:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:52:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:53:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:53:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:53:03 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:53:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678889645a4645e6df6f5951b2faa756bcfc3a1c3a4d8b70126c8a381970e38`  
		Last Modified: Sat, 16 Oct 2021 03:53:30 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efc1be380cbc922ab4999aadde7b6c48c5228b757176209810d37554b2a056`  
		Last Modified: Sat, 16 Oct 2021 03:53:29 GMT  
		Size: 4.3 MB (4261579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d08baf1e962da42289483767cf16f450fa53b811b8ea12fcb586456118c231`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 3.2 MB (3207277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4740e2a70f5d2095f3d51954350c8e36372bfdf44b299200782ef6400531492`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d60a563e61658b2baa5c9a39817163d2495b9b95287924ce4df038e04064`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 1.5 MB (1529514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69340b12ab80abf3c9554baf7c743d8791a0d45fbbc9f2c7efefd4cfff119e`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5642e3f068c45be659c51cbca4d39a50fe31c60ec80358a64dc472e0eff1f5`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1cb90f79536f885082931f544d2493e28e994955deb5c3973f8efbcbe2e51`  
		Last Modified: Wed, 10 Nov 2021 00:57:05 GMT  
		Size: 71.5 MB (71495396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447a2046003f9b2338245d6ad83415cfac5530e4a9d96e874630928f08cb9cb`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d14c8dc2043c7306e2cac5e1e53f3dd2319ff5a5e5df8c5e116cc4daccabbe9`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aaa29bc3bab3a7aec9637991fbb009ab4524376f77d44750ec7601e3293f0c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117698933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83f8127b7c2500d881d29a5e4a43d45de6f693be38acf616e6b43d41bcdd4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:10:39 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 03:11:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 03:12:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 03:12:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:12:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 03:12:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:13:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:14 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:19 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 03:13:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:15:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:15:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:15:54 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:16:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:16:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:16:10 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:16:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d1b9e80c0330e70eec7e4746217b26e14d1a9e97a03bff51a6acf663a75a10`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 3.5 MB (3533213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927db937b773bb118edcd41e143a4b75710e7e45d1ebc181360edfa4a87818e7`  
		Last Modified: Wed, 10 Nov 2021 03:20:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3d24ccb97f9776893abffce060cc28690f9bafff16116a409e1bc224eb4356`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 1.9 MB (1937102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f83a0eeaf9b0378ef5be732c550cc019b529be4c9dad720f1aa6166b591e573`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9b0819ad891f7f8ac18418d3ddfb8265cd19728ed79ad2eb33e16e14a8136a`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e322340ec7651facf5e69b97fff295833396435f911081455778e986918f1`  
		Last Modified: Wed, 10 Nov 2021 03:21:10 GMT  
		Size: 76.2 MB (76152088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2d96724ea50492970d4833e3d6041f1c0999a3c8e38658a9ea49a0981eeb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d35b0dfeb42e74c605540f01f745397b7b8968ee399c173cd74c9726e68472`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41`

```console
$ docker pull mariadb@sha256:3a4ab2d232d68eda6c02ac21b3d0117ba6826422095ffa19c7cc2947833dc3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41` - linux; amd64

```console
$ docker pull mariadb@sha256:9f3d32d94acf1575778352a57736b8658b2e82914c95132e17cbae972ddd75d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109366470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da013e07658f467ba302052e465953694726c99953a0dc9a156a5607a984174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:14 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:32:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:32:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:32:49 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:32:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 01:33:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:33:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:33:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:33:43 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:33:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:33:44 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:33:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa82e4a480b0031196004180195fe405a9be3b3aa27b3a5707496385917e6f`  
		Last Modified: Wed, 10 Nov 2021 01:36:54 GMT  
		Size: 3.6 MB (3552876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8dfea7939d5fdf3afaf0e79ea3381ba8fa5be197d5e021c3cafb5444f7c90`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1650ff0f0b14f377b4cd4062abc5a68952d6cd4d96a445186049b6da8389f`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 1.6 MB (1583644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbbf5c0a7a156c68beab396f0f6a5c49f27d57afb630cab06111863ef3c0a04`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da10f864031144349b7bb74f484e2f733cf52c68f4346fb3dfe93438f4265c8e`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588fb2eae01fe7432714c5cd41cabc95d3e523000ae6788ee8900a98ad51eac`  
		Last Modified: Wed, 10 Nov 2021 01:37:01 GMT  
		Size: 72.7 MB (72698371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f7de3033fe99fc9691f6e3c6d70a829e5370bba6aa226a7701c2e826e9740c`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2edfd564b64d5f9d965e2380937a281db0aa8ff4e9152384de33a2c59cbc71`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:448a233b8d75def87d6db6cd6623a2042c1d9b97bba0d641a3f4988603a46d89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf901a92a5d2bc9cc1508a8d8a697d32b1fcf98a720b7473c710d5ca153ca69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:38 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Sat, 16 Oct 2021 01:47:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:48:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:49:08 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:51:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:52:06 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:52:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:52:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:52:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:52:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:52:22 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:24 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:25 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 00:52:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:52:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:52:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:53:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:53:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:53:03 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:53:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678889645a4645e6df6f5951b2faa756bcfc3a1c3a4d8b70126c8a381970e38`  
		Last Modified: Sat, 16 Oct 2021 03:53:30 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efc1be380cbc922ab4999aadde7b6c48c5228b757176209810d37554b2a056`  
		Last Modified: Sat, 16 Oct 2021 03:53:29 GMT  
		Size: 4.3 MB (4261579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d08baf1e962da42289483767cf16f450fa53b811b8ea12fcb586456118c231`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 3.2 MB (3207277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4740e2a70f5d2095f3d51954350c8e36372bfdf44b299200782ef6400531492`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d60a563e61658b2baa5c9a39817163d2495b9b95287924ce4df038e04064`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 1.5 MB (1529514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69340b12ab80abf3c9554baf7c743d8791a0d45fbbc9f2c7efefd4cfff119e`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5642e3f068c45be659c51cbca4d39a50fe31c60ec80358a64dc472e0eff1f5`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1cb90f79536f885082931f544d2493e28e994955deb5c3973f8efbcbe2e51`  
		Last Modified: Wed, 10 Nov 2021 00:57:05 GMT  
		Size: 71.5 MB (71495396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447a2046003f9b2338245d6ad83415cfac5530e4a9d96e874630928f08cb9cb`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d14c8dc2043c7306e2cac5e1e53f3dd2319ff5a5e5df8c5e116cc4daccabbe9`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aaa29bc3bab3a7aec9637991fbb009ab4524376f77d44750ec7601e3293f0c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117698933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83f8127b7c2500d881d29a5e4a43d45de6f693be38acf616e6b43d41bcdd4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:10:39 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 03:11:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 03:12:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 03:12:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:12:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 03:12:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:13:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:14 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:19 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 03:13:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:15:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:15:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:15:54 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:16:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:16:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:16:10 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:16:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d1b9e80c0330e70eec7e4746217b26e14d1a9e97a03bff51a6acf663a75a10`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 3.5 MB (3533213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927db937b773bb118edcd41e143a4b75710e7e45d1ebc181360edfa4a87818e7`  
		Last Modified: Wed, 10 Nov 2021 03:20:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3d24ccb97f9776893abffce060cc28690f9bafff16116a409e1bc224eb4356`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 1.9 MB (1937102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f83a0eeaf9b0378ef5be732c550cc019b529be4c9dad720f1aa6166b591e573`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9b0819ad891f7f8ac18418d3ddfb8265cd19728ed79ad2eb33e16e14a8136a`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e322340ec7651facf5e69b97fff295833396435f911081455778e986918f1`  
		Last Modified: Wed, 10 Nov 2021 03:21:10 GMT  
		Size: 76.2 MB (76152088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2d96724ea50492970d4833e3d6041f1c0999a3c8e38658a9ea49a0981eeb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d35b0dfeb42e74c605540f01f745397b7b8968ee399c173cd74c9726e68472`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41-bionic`

```console
$ docker pull mariadb@sha256:3a4ab2d232d68eda6c02ac21b3d0117ba6826422095ffa19c7cc2947833dc3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:9f3d32d94acf1575778352a57736b8658b2e82914c95132e17cbae972ddd75d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109366470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da013e07658f467ba302052e465953694726c99953a0dc9a156a5607a984174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:22:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Oct 2021 05:22:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:14 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:32:39 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:32:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:32:49 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:32:49 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:32:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 01:32:59 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 01:32:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 01:33:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:33:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:33:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:33:43 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:33:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:33:44 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:33:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939c6256f1f0a750da3d02b63d4aa63b9ac6f085a5b904ede35065e2f9074ad`  
		Last Modified: Fri, 01 Oct 2021 05:26:25 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b11a4bc2affe5918649c7ac2245c1ba21dc9f4ea8a536f01188e6e7a32bf30`  
		Last Modified: Fri, 01 Oct 2021 05:26:24 GMT  
		Size: 4.8 MB (4813381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa82e4a480b0031196004180195fe405a9be3b3aa27b3a5707496385917e6f`  
		Last Modified: Wed, 10 Nov 2021 01:36:54 GMT  
		Size: 3.6 MB (3552876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8dfea7939d5fdf3afaf0e79ea3381ba8fa5be197d5e021c3cafb5444f7c90`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1650ff0f0b14f377b4cd4062abc5a68952d6cd4d96a445186049b6da8389f`  
		Last Modified: Wed, 10 Nov 2021 01:36:53 GMT  
		Size: 1.6 MB (1583644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbbf5c0a7a156c68beab396f0f6a5c49f27d57afb630cab06111863ef3c0a04`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da10f864031144349b7bb74f484e2f733cf52c68f4346fb3dfe93438f4265c8e`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588fb2eae01fe7432714c5cd41cabc95d3e523000ae6788ee8900a98ad51eac`  
		Last Modified: Wed, 10 Nov 2021 01:37:01 GMT  
		Size: 72.7 MB (72698371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f7de3033fe99fc9691f6e3c6d70a829e5370bba6aa226a7701c2e826e9740c`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2edfd564b64d5f9d965e2380937a281db0aa8ff4e9152384de33a2c59cbc71`  
		Last Modified: Wed, 10 Nov 2021 01:36:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:448a233b8d75def87d6db6cd6623a2042c1d9b97bba0d641a3f4988603a46d89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104234437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf901a92a5d2bc9cc1508a8d8a697d32b1fcf98a720b7473c710d5ca153ca69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:38 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Sat, 16 Oct 2021 01:47:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:48:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:49:08 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:51:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:52:06 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:52:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:52:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:52:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:52:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:52:22 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 00:52:24 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:25 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 00:52:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 00:52:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:52:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:52:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:53:01 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:53:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:53:03 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:53:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678889645a4645e6df6f5951b2faa756bcfc3a1c3a4d8b70126c8a381970e38`  
		Last Modified: Sat, 16 Oct 2021 03:53:30 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efc1be380cbc922ab4999aadde7b6c48c5228b757176209810d37554b2a056`  
		Last Modified: Sat, 16 Oct 2021 03:53:29 GMT  
		Size: 4.3 MB (4261579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d08baf1e962da42289483767cf16f450fa53b811b8ea12fcb586456118c231`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 3.2 MB (3207277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4740e2a70f5d2095f3d51954350c8e36372bfdf44b299200782ef6400531492`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d60a563e61658b2baa5c9a39817163d2495b9b95287924ce4df038e04064`  
		Last Modified: Wed, 10 Nov 2021 00:56:56 GMT  
		Size: 1.5 MB (1529514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69340b12ab80abf3c9554baf7c743d8791a0d45fbbc9f2c7efefd4cfff119e`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5642e3f068c45be659c51cbca4d39a50fe31c60ec80358a64dc472e0eff1f5`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1cb90f79536f885082931f544d2493e28e994955deb5c3973f8efbcbe2e51`  
		Last Modified: Wed, 10 Nov 2021 00:57:05 GMT  
		Size: 71.5 MB (71495396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447a2046003f9b2338245d6ad83415cfac5530e4a9d96e874630928f08cb9cb`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d14c8dc2043c7306e2cac5e1e53f3dd2319ff5a5e5df8c5e116cc4daccabbe9`  
		Last Modified: Wed, 10 Nov 2021 00:56:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:aaa29bc3bab3a7aec9637991fbb009ab4524376f77d44750ec7601e3293f0c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117698933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83f8127b7c2500d881d29a5e4a43d45de6f693be38acf616e6b43d41bcdd4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 18:27:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Oct 2021 18:28:04 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:10:39 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 03:11:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 03:12:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 03:12:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:12:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 03:12:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:13:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 10 Nov 2021 03:13:14 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:19 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 10 Nov 2021 03:13:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 10 Nov 2021 03:13:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:15:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:15:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:15:54 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:16:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:16:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:16:10 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:16:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508be09c006b6365ae7c5fc9b0593010a2d284d9b02e4f9ad77ee4f4209c8c0a`  
		Last Modified: Wed, 06 Oct 2021 18:37:35 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc7004e2371a404c5ff023b89e2ade70ef3581e3c7156807ac620fad13dbaf`  
		Last Modified: Wed, 06 Oct 2021 18:37:32 GMT  
		Size: 5.6 MB (5630476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d1b9e80c0330e70eec7e4746217b26e14d1a9e97a03bff51a6acf663a75a10`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 3.5 MB (3533213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927db937b773bb118edcd41e143a4b75710e7e45d1ebc181360edfa4a87818e7`  
		Last Modified: Wed, 10 Nov 2021 03:20:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3d24ccb97f9776893abffce060cc28690f9bafff16116a409e1bc224eb4356`  
		Last Modified: Wed, 10 Nov 2021 03:20:59 GMT  
		Size: 1.9 MB (1937102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f83a0eeaf9b0378ef5be732c550cc019b529be4c9dad720f1aa6166b591e573`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9b0819ad891f7f8ac18418d3ddfb8265cd19728ed79ad2eb33e16e14a8136a`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e322340ec7651facf5e69b97fff295833396435f911081455778e986918f1`  
		Last Modified: Wed, 10 Nov 2021 03:21:10 GMT  
		Size: 76.2 MB (76152088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2d96724ea50492970d4833e3d6041f1c0999a3c8e38658a9ea49a0981eeb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d35b0dfeb42e74c605540f01f745397b7b8968ee399c173cd74c9726e68472`  
		Last Modified: Wed, 10 Nov 2021 03:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:bcdd46c80909609f7e496528cdaa02c4bd493f14a7e61400cfcb4fc2fcf39143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:cd33a9afb2e44071e6bb3aee07a3552ce99b350f4bdcff7673bc568dd32160e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120122963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77d7ce2134c9c69d50f9031ab98edabe542091b9378bb06265d047054b86420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:32:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:32:10 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:32:10 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:32:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:32:11 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:32:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0d131753ad8682f71eee1229a2d59c5f96d9875e508e2386d17717b1713a96`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a25510678007841a718455c14be13bf4c871f86987b73ca8daa470da405ef93`  
		Last Modified: Wed, 10 Nov 2021 01:36:35 GMT  
		Size: 80.2 MB (80197070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb86de5e3bb1b3d39ca337f205a247ad7d9b0942158fdd7ce4c8c1332a9881`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472822fb9afa73d662c822df3f8a6b83a48be60e6de82536b5d1a79842c4547`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7edf766e697b595aa47bc77fd7b223fdd47b2733d02d51c42db20f0f975c136b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef55b042142902be1eea435e69b38b707498fb6e5fe04a1d7c953b1c52842e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:50:47 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:49 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:50 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:50:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:51:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:51:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:51:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:51:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:51:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a8d5aee569f5ae47a3c8525b74300ca8dbf60841037717a9d0eacd54de432`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449bdf279e936efac03b48459f8615318e06f7ef3541788ad85d5acc644bc716`  
		Last Modified: Wed, 10 Nov 2021 00:56:36 GMT  
		Size: 79.5 MB (79529598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f5f24cc6c2c6e39831c31f2ff45b3de01abae6e5ae7f0f69c4b30e28d2986`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ca38d6c27164fc4d2fc76801456929a94d015fc3da882cf0c935dca63bb069`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f45b5ee7c40f6b2e777ab9e4114aeecf6d2320d340eecb498bdcf953acdc187
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130999404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a077eb8e726e7763173be24500692bb66de82b91f0498fc96c347a22807d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:07:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:45 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:47 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:49 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:07:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:10:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:10:02 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:10:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:10:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:10:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:10:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a18c89cf16c66aee1426ea78e2801e12dd4064d7c2a9d0155bb3a987443aee2`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2563e58558c56d117b0bfe5a87b1b1449fd6897fdba8ab4bbf7f33e0561aafb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:36 GMT  
		Size: 84.8 MB (84791253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e09ef8f27fcecb76404b910773a1f4d4cfc94c7ca72bf17d50089638a8f7cc4`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a6d9c9473adc10a12565ddbbf98490b285c7f00da9b4adc4beeb6f5bb230b`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:bcdd46c80909609f7e496528cdaa02c4bd493f14a7e61400cfcb4fc2fcf39143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:cd33a9afb2e44071e6bb3aee07a3552ce99b350f4bdcff7673bc568dd32160e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120122963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77d7ce2134c9c69d50f9031ab98edabe542091b9378bb06265d047054b86420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:32:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:32:10 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:32:10 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:32:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:32:11 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:32:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0d131753ad8682f71eee1229a2d59c5f96d9875e508e2386d17717b1713a96`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a25510678007841a718455c14be13bf4c871f86987b73ca8daa470da405ef93`  
		Last Modified: Wed, 10 Nov 2021 01:36:35 GMT  
		Size: 80.2 MB (80197070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb86de5e3bb1b3d39ca337f205a247ad7d9b0942158fdd7ce4c8c1332a9881`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472822fb9afa73d662c822df3f8a6b83a48be60e6de82536b5d1a79842c4547`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7edf766e697b595aa47bc77fd7b223fdd47b2733d02d51c42db20f0f975c136b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef55b042142902be1eea435e69b38b707498fb6e5fe04a1d7c953b1c52842e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:50:47 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:49 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:50 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:50:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:51:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:51:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:51:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:51:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:51:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a8d5aee569f5ae47a3c8525b74300ca8dbf60841037717a9d0eacd54de432`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449bdf279e936efac03b48459f8615318e06f7ef3541788ad85d5acc644bc716`  
		Last Modified: Wed, 10 Nov 2021 00:56:36 GMT  
		Size: 79.5 MB (79529598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f5f24cc6c2c6e39831c31f2ff45b3de01abae6e5ae7f0f69c4b30e28d2986`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ca38d6c27164fc4d2fc76801456929a94d015fc3da882cf0c935dca63bb069`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f45b5ee7c40f6b2e777ab9e4114aeecf6d2320d340eecb498bdcf953acdc187
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130999404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a077eb8e726e7763173be24500692bb66de82b91f0498fc96c347a22807d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:07:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:45 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:47 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:49 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:07:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:10:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:10:02 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:10:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:10:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:10:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:10:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a18c89cf16c66aee1426ea78e2801e12dd4064d7c2a9d0155bb3a987443aee2`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2563e58558c56d117b0bfe5a87b1b1449fd6897fdba8ab4bbf7f33e0561aafb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:36 GMT  
		Size: 84.8 MB (84791253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e09ef8f27fcecb76404b910773a1f4d4cfc94c7ca72bf17d50089638a8f7cc4`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a6d9c9473adc10a12565ddbbf98490b285c7f00da9b4adc4beeb6f5bb230b`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32`

```console
$ docker pull mariadb@sha256:bcdd46c80909609f7e496528cdaa02c4bd493f14a7e61400cfcb4fc2fcf39143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32` - linux; amd64

```console
$ docker pull mariadb@sha256:cd33a9afb2e44071e6bb3aee07a3552ce99b350f4bdcff7673bc568dd32160e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120122963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77d7ce2134c9c69d50f9031ab98edabe542091b9378bb06265d047054b86420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:32:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:32:10 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:32:10 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:32:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:32:11 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:32:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0d131753ad8682f71eee1229a2d59c5f96d9875e508e2386d17717b1713a96`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a25510678007841a718455c14be13bf4c871f86987b73ca8daa470da405ef93`  
		Last Modified: Wed, 10 Nov 2021 01:36:35 GMT  
		Size: 80.2 MB (80197070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb86de5e3bb1b3d39ca337f205a247ad7d9b0942158fdd7ce4c8c1332a9881`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472822fb9afa73d662c822df3f8a6b83a48be60e6de82536b5d1a79842c4547`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7edf766e697b595aa47bc77fd7b223fdd47b2733d02d51c42db20f0f975c136b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef55b042142902be1eea435e69b38b707498fb6e5fe04a1d7c953b1c52842e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:50:47 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:49 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:50 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:50:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:51:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:51:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:51:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:51:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:51:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a8d5aee569f5ae47a3c8525b74300ca8dbf60841037717a9d0eacd54de432`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449bdf279e936efac03b48459f8615318e06f7ef3541788ad85d5acc644bc716`  
		Last Modified: Wed, 10 Nov 2021 00:56:36 GMT  
		Size: 79.5 MB (79529598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f5f24cc6c2c6e39831c31f2ff45b3de01abae6e5ae7f0f69c4b30e28d2986`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ca38d6c27164fc4d2fc76801456929a94d015fc3da882cf0c935dca63bb069`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f45b5ee7c40f6b2e777ab9e4114aeecf6d2320d340eecb498bdcf953acdc187
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130999404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a077eb8e726e7763173be24500692bb66de82b91f0498fc96c347a22807d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:07:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:45 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:47 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:49 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:07:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:10:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:10:02 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:10:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:10:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:10:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:10:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a18c89cf16c66aee1426ea78e2801e12dd4064d7c2a9d0155bb3a987443aee2`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2563e58558c56d117b0bfe5a87b1b1449fd6897fdba8ab4bbf7f33e0561aafb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:36 GMT  
		Size: 84.8 MB (84791253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e09ef8f27fcecb76404b910773a1f4d4cfc94c7ca72bf17d50089638a8f7cc4`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a6d9c9473adc10a12565ddbbf98490b285c7f00da9b4adc4beeb6f5bb230b`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32-focal`

```console
$ docker pull mariadb@sha256:bcdd46c80909609f7e496528cdaa02c4bd493f14a7e61400cfcb4fc2fcf39143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:cd33a9afb2e44071e6bb3aee07a3552ce99b350f4bdcff7673bc568dd32160e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120122963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77d7ce2134c9c69d50f9031ab98edabe542091b9378bb06265d047054b86420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 01:31:41 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 01:31:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:32:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:32:10 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:32:10 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:32:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:32:11 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:32:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0d131753ad8682f71eee1229a2d59c5f96d9875e508e2386d17717b1713a96`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a25510678007841a718455c14be13bf4c871f86987b73ca8daa470da405ef93`  
		Last Modified: Wed, 10 Nov 2021 01:36:35 GMT  
		Size: 80.2 MB (80197070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb86de5e3bb1b3d39ca337f205a247ad7d9b0942158fdd7ce4c8c1332a9881`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472822fb9afa73d662c822df3f8a6b83a48be60e6de82536b5d1a79842c4547`  
		Last Modified: Wed, 10 Nov 2021 01:36:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7edf766e697b595aa47bc77fd7b223fdd47b2733d02d51c42db20f0f975c136b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef55b042142902be1eea435e69b38b707498fb6e5fe04a1d7c953b1c52842e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:50:47 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 00:50:49 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:50 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 00:50:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:50:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:51:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:51:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:51:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:51:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:51:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a8d5aee569f5ae47a3c8525b74300ca8dbf60841037717a9d0eacd54de432`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449bdf279e936efac03b48459f8615318e06f7ef3541788ad85d5acc644bc716`  
		Last Modified: Wed, 10 Nov 2021 00:56:36 GMT  
		Size: 79.5 MB (79529598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f5f24cc6c2c6e39831c31f2ff45b3de01abae6e5ae7f0f69c4b30e28d2986`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ca38d6c27164fc4d2fc76801456929a94d015fc3da882cf0c935dca63bb069`  
		Last Modified: Wed, 10 Nov 2021 00:56:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f45b5ee7c40f6b2e777ab9e4114aeecf6d2320d340eecb498bdcf953acdc187
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130999404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a077eb8e726e7763173be24500692bb66de82b91f0498fc96c347a22807d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:07:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:45 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 10 Nov 2021 03:07:47 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:49 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 10 Nov 2021 03:07:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:07:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:10:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:10:02 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:10:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:10:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:10:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:10:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a18c89cf16c66aee1426ea78e2801e12dd4064d7c2a9d0155bb3a987443aee2`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2563e58558c56d117b0bfe5a87b1b1449fd6897fdba8ab4bbf7f33e0561aafb1`  
		Last Modified: Wed, 10 Nov 2021 03:20:36 GMT  
		Size: 84.8 MB (84791253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e09ef8f27fcecb76404b910773a1f4d4cfc94c7ca72bf17d50089638a8f7cc4`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a6d9c9473adc10a12565ddbbf98490b285c7f00da9b4adc4beeb6f5bb230b`  
		Last Modified: Wed, 10 Nov 2021 03:20:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:ba48fe2ec6c6ca2fd960144c6e3415570fe7a5c461487244ab2973651c4e8bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:b2bc5247ac4cea39d672a8a76b677d78763e8960135fa1740f46ee457c051457
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124844178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ceee7cde5e0d9b1d1edb9ae019076a852f94ab03bc7594133122abcb3f316b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:33 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059a6a94b785691c0d9ec1363f821f0a01865091a5573a23663d8e01dd08dab9`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7193d128be6822df99863f70eca65ba3e3221043294d0892ce7bfeaf3eb5080b`  
		Last Modified: Wed, 10 Nov 2021 01:36:07 GMT  
		Size: 84.9 MB (84918282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c515c1f53468252f9dc7a070c74db33297ad9cdf0f1d92e9f20c56825dafe`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbd919c30d066f3d73096450b4eb69fa6895385b986d8ab6659985c46916cf6`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f5d97fe32efba4fcabc0c50fb279baca200a24d7bd3c6c5eab6a5c8a55546d51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122266711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b114c0197caae0ae0b6719e98be4c9c2ed0b028de3ea7f3c482a9843fac06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:46 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:48 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:49 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:50:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:50:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:50:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:50:40 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:50:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c164e3ca68304b78e43d60989b86cd1767bf513697222b261bfae695369f4a1c`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40938e19154abd8263b6386908314129e10ea50ef51c72ff715f046d5055c869`  
		Last Modified: Wed, 10 Nov 2021 00:56:06 GMT  
		Size: 84.2 MB (84190611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c5db793f079be68f6ed2d4b51340a29241819ebcdd22e84ac211d0b1f25efb`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dce99c002092df9573d3ed620422a4173840c4a051834bb32c580a18f5924b`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cf618ae1b7a01583c20c8e1be97454402092de7f3d0153481f7d2246be2983a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135606413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dc974cc24d1673dad9e2481a8f9e41c9da9f641d5e8d0c4c3e0dfa0272fd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:04:03 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:07 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:10 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:13 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:04:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:06:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:07:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:07:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:07:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:07:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:07:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:07:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2d8cdb436daa4a878149d007a35cbbf6127da194963ef60cc4f91c88576a73`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644d600ff6fca91d4d45170e0325b5165497cb5e59c8e9035998d8676ffacbe6`  
		Last Modified: Wed, 10 Nov 2021 03:19:57 GMT  
		Size: 89.4 MB (89398264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2183805272408c6188591a40671b6c41242f32e69644c320c077f2f81796fb6`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4492eb5cdda581483ea325081f8c68872ec1cf00be709cab0259be134e0e6a`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:ba48fe2ec6c6ca2fd960144c6e3415570fe7a5c461487244ab2973651c4e8bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b2bc5247ac4cea39d672a8a76b677d78763e8960135fa1740f46ee457c051457
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124844178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ceee7cde5e0d9b1d1edb9ae019076a852f94ab03bc7594133122abcb3f316b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:33 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059a6a94b785691c0d9ec1363f821f0a01865091a5573a23663d8e01dd08dab9`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7193d128be6822df99863f70eca65ba3e3221043294d0892ce7bfeaf3eb5080b`  
		Last Modified: Wed, 10 Nov 2021 01:36:07 GMT  
		Size: 84.9 MB (84918282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c515c1f53468252f9dc7a070c74db33297ad9cdf0f1d92e9f20c56825dafe`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbd919c30d066f3d73096450b4eb69fa6895385b986d8ab6659985c46916cf6`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f5d97fe32efba4fcabc0c50fb279baca200a24d7bd3c6c5eab6a5c8a55546d51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122266711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b114c0197caae0ae0b6719e98be4c9c2ed0b028de3ea7f3c482a9843fac06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:46 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:48 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:49 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:50:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:50:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:50:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:50:40 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:50:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c164e3ca68304b78e43d60989b86cd1767bf513697222b261bfae695369f4a1c`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40938e19154abd8263b6386908314129e10ea50ef51c72ff715f046d5055c869`  
		Last Modified: Wed, 10 Nov 2021 00:56:06 GMT  
		Size: 84.2 MB (84190611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c5db793f079be68f6ed2d4b51340a29241819ebcdd22e84ac211d0b1f25efb`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dce99c002092df9573d3ed620422a4173840c4a051834bb32c580a18f5924b`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cf618ae1b7a01583c20c8e1be97454402092de7f3d0153481f7d2246be2983a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135606413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dc974cc24d1673dad9e2481a8f9e41c9da9f641d5e8d0c4c3e0dfa0272fd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:04:03 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:07 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:10 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:13 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:04:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:06:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:07:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:07:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:07:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:07:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:07:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:07:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2d8cdb436daa4a878149d007a35cbbf6127da194963ef60cc4f91c88576a73`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644d600ff6fca91d4d45170e0325b5165497cb5e59c8e9035998d8676ffacbe6`  
		Last Modified: Wed, 10 Nov 2021 03:19:57 GMT  
		Size: 89.4 MB (89398264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2183805272408c6188591a40671b6c41242f32e69644c320c077f2f81796fb6`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4492eb5cdda581483ea325081f8c68872ec1cf00be709cab0259be134e0e6a`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22`

```console
$ docker pull mariadb@sha256:ba48fe2ec6c6ca2fd960144c6e3415570fe7a5c461487244ab2973651c4e8bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22` - linux; amd64

```console
$ docker pull mariadb@sha256:b2bc5247ac4cea39d672a8a76b677d78763e8960135fa1740f46ee457c051457
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124844178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ceee7cde5e0d9b1d1edb9ae019076a852f94ab03bc7594133122abcb3f316b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:33 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059a6a94b785691c0d9ec1363f821f0a01865091a5573a23663d8e01dd08dab9`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7193d128be6822df99863f70eca65ba3e3221043294d0892ce7bfeaf3eb5080b`  
		Last Modified: Wed, 10 Nov 2021 01:36:07 GMT  
		Size: 84.9 MB (84918282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c515c1f53468252f9dc7a070c74db33297ad9cdf0f1d92e9f20c56825dafe`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbd919c30d066f3d73096450b4eb69fa6895385b986d8ab6659985c46916cf6`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f5d97fe32efba4fcabc0c50fb279baca200a24d7bd3c6c5eab6a5c8a55546d51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122266711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b114c0197caae0ae0b6719e98be4c9c2ed0b028de3ea7f3c482a9843fac06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:46 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:48 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:49 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:50:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:50:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:50:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:50:40 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:50:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c164e3ca68304b78e43d60989b86cd1767bf513697222b261bfae695369f4a1c`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40938e19154abd8263b6386908314129e10ea50ef51c72ff715f046d5055c869`  
		Last Modified: Wed, 10 Nov 2021 00:56:06 GMT  
		Size: 84.2 MB (84190611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c5db793f079be68f6ed2d4b51340a29241819ebcdd22e84ac211d0b1f25efb`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dce99c002092df9573d3ed620422a4173840c4a051834bb32c580a18f5924b`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cf618ae1b7a01583c20c8e1be97454402092de7f3d0153481f7d2246be2983a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135606413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dc974cc24d1673dad9e2481a8f9e41c9da9f641d5e8d0c4c3e0dfa0272fd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:04:03 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:07 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:10 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:13 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:04:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:06:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:07:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:07:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:07:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:07:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:07:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:07:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2d8cdb436daa4a878149d007a35cbbf6127da194963ef60cc4f91c88576a73`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644d600ff6fca91d4d45170e0325b5165497cb5e59c8e9035998d8676ffacbe6`  
		Last Modified: Wed, 10 Nov 2021 03:19:57 GMT  
		Size: 89.4 MB (89398264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2183805272408c6188591a40671b6c41242f32e69644c320c077f2f81796fb6`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4492eb5cdda581483ea325081f8c68872ec1cf00be709cab0259be134e0e6a`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22-focal`

```console
$ docker pull mariadb@sha256:ba48fe2ec6c6ca2fd960144c6e3415570fe7a5c461487244ab2973651c4e8bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b2bc5247ac4cea39d672a8a76b677d78763e8960135fa1740f46ee457c051457
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124844178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ceee7cde5e0d9b1d1edb9ae019076a852f94ab03bc7594133122abcb3f316b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 01:31:08 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:08 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 01:31:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:31:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:33 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 01:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:34 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059a6a94b785691c0d9ec1363f821f0a01865091a5573a23663d8e01dd08dab9`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7193d128be6822df99863f70eca65ba3e3221043294d0892ce7bfeaf3eb5080b`  
		Last Modified: Wed, 10 Nov 2021 01:36:07 GMT  
		Size: 84.9 MB (84918282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c515c1f53468252f9dc7a070c74db33297ad9cdf0f1d92e9f20c56825dafe`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbd919c30d066f3d73096450b4eb69fa6895385b986d8ab6659985c46916cf6`  
		Last Modified: Wed, 10 Nov 2021 01:35:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f5d97fe32efba4fcabc0c50fb279baca200a24d7bd3c6c5eab6a5c8a55546d51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122266711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b114c0197caae0ae0b6719e98be4c9c2ed0b028de3ea7f3c482a9843fac06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:46 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 00:49:48 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:49 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 00:49:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:50:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:50:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:50:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 00:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:50:40 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:50:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c164e3ca68304b78e43d60989b86cd1767bf513697222b261bfae695369f4a1c`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40938e19154abd8263b6386908314129e10ea50ef51c72ff715f046d5055c869`  
		Last Modified: Wed, 10 Nov 2021 00:56:06 GMT  
		Size: 84.2 MB (84190611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c5db793f079be68f6ed2d4b51340a29241819ebcdd22e84ac211d0b1f25efb`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dce99c002092df9573d3ed620422a4173840c4a051834bb32c580a18f5924b`  
		Last Modified: Wed, 10 Nov 2021 00:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cf618ae1b7a01583c20c8e1be97454402092de7f3d0153481f7d2246be2983a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135606413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dc974cc24d1673dad9e2481a8f9e41c9da9f641d5e8d0c4c3e0dfa0272fd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:04:03 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:07 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 10 Nov 2021 03:04:10 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:13 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 10 Nov 2021 03:04:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:04:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:06:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:07:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:07:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:07:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 10 Nov 2021 03:07:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:07:23 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:07:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2d8cdb436daa4a878149d007a35cbbf6127da194963ef60cc4f91c88576a73`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644d600ff6fca91d4d45170e0325b5165497cb5e59c8e9035998d8676ffacbe6`  
		Last Modified: Wed, 10 Nov 2021 03:19:57 GMT  
		Size: 89.4 MB (89398264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2183805272408c6188591a40671b6c41242f32e69644c320c077f2f81796fb6`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 5.6 KB (5624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4492eb5cdda581483ea325081f8c68872ec1cf00be709cab0259be134e0e6a`  
		Last Modified: Wed, 10 Nov 2021 03:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:8abb0ddefb8408d1f62553edef61756ad9e8598f475082f5f5ca89b8807b2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:978c7269e9db8dd4b1a99f6113cab668ebd7b17d44238979967d73eb8872c655
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127018178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e59bdf6f04475b9c3b17dd48dd9da27860cbba9ef57ed7c6b0b0d3d462a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:04 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0b425c6060ca5500da6904b6bcd19e871ed8940155c1ff657524b22c9b925`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9241e174f72407715b034a6bae613e6ed1545f915365c405fae15998ece063db`  
		Last Modified: Wed, 10 Nov 2021 01:35:40 GMT  
		Size: 87.1 MB (87092406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35766610697c5332b1b79fc29ba7db6daa466ab9c461e0cb4b04c5fb88836940`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c55628364c58dd74d453efea996264c328e8d3ac57265dd8ca46741ace07702b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ac0020779a37b67674a9e7966eb3b53e365f1c9a9a1200a39bb6e8c9a0855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:02 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:03 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:04 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:05 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:49:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:49:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:49:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:49:39 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c71db2ec96091d918177b4caba5b8c2d89d3f78fef4eafc7ac9be00b4ec481`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28091fd75396522470a3f6501951a656411bc0380177cb74c6a86e9a10bb0457`  
		Last Modified: Wed, 10 Nov 2021 00:55:35 GMT  
		Size: 86.2 MB (86227517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9813b2cee15453f70ae9749381a1e97b8c46f9cdfa6df02d91156d46768fd0ce`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ae9fa988b63ceabfed0bdf0b7c20d9ae9606d6e93a36adc4c994849b3ea71a5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53777ed29e137e916ca6efb0b9a3f9708d5f2eb56ec8916037184765b8a58d57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:00:22 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:26 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:28 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:32 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:00:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:03:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:03:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:03:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:03:32 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:03:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253bbb84fa1eea425ed4f73f19a49bd742c24720031613e1fe123947d7fe5440`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d297f3097b64e102365b90a52a234c536ff3deb43a9c003e376b31fb2bd2`  
		Last Modified: Wed, 10 Nov 2021 03:19:20 GMT  
		Size: 91.5 MB (91540848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3794fb4895a5a92d49914af625d8427af1213db3d582df0fbdcf10c58e8b6550`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:8abb0ddefb8408d1f62553edef61756ad9e8598f475082f5f5ca89b8807b2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:978c7269e9db8dd4b1a99f6113cab668ebd7b17d44238979967d73eb8872c655
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127018178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e59bdf6f04475b9c3b17dd48dd9da27860cbba9ef57ed7c6b0b0d3d462a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:04 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0b425c6060ca5500da6904b6bcd19e871ed8940155c1ff657524b22c9b925`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9241e174f72407715b034a6bae613e6ed1545f915365c405fae15998ece063db`  
		Last Modified: Wed, 10 Nov 2021 01:35:40 GMT  
		Size: 87.1 MB (87092406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35766610697c5332b1b79fc29ba7db6daa466ab9c461e0cb4b04c5fb88836940`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c55628364c58dd74d453efea996264c328e8d3ac57265dd8ca46741ace07702b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ac0020779a37b67674a9e7966eb3b53e365f1c9a9a1200a39bb6e8c9a0855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:02 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:03 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:04 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:05 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:49:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:49:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:49:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:49:39 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c71db2ec96091d918177b4caba5b8c2d89d3f78fef4eafc7ac9be00b4ec481`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28091fd75396522470a3f6501951a656411bc0380177cb74c6a86e9a10bb0457`  
		Last Modified: Wed, 10 Nov 2021 00:55:35 GMT  
		Size: 86.2 MB (86227517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9813b2cee15453f70ae9749381a1e97b8c46f9cdfa6df02d91156d46768fd0ce`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ae9fa988b63ceabfed0bdf0b7c20d9ae9606d6e93a36adc4c994849b3ea71a5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53777ed29e137e916ca6efb0b9a3f9708d5f2eb56ec8916037184765b8a58d57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:00:22 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:26 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:28 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:32 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:00:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:03:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:03:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:03:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:03:32 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:03:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253bbb84fa1eea425ed4f73f19a49bd742c24720031613e1fe123947d7fe5440`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d297f3097b64e102365b90a52a234c536ff3deb43a9c003e376b31fb2bd2`  
		Last Modified: Wed, 10 Nov 2021 03:19:20 GMT  
		Size: 91.5 MB (91540848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3794fb4895a5a92d49914af625d8427af1213db3d582df0fbdcf10c58e8b6550`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:8abb0ddefb8408d1f62553edef61756ad9e8598f475082f5f5ca89b8807b2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13` - linux; amd64

```console
$ docker pull mariadb@sha256:978c7269e9db8dd4b1a99f6113cab668ebd7b17d44238979967d73eb8872c655
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127018178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e59bdf6f04475b9c3b17dd48dd9da27860cbba9ef57ed7c6b0b0d3d462a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:04 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0b425c6060ca5500da6904b6bcd19e871ed8940155c1ff657524b22c9b925`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9241e174f72407715b034a6bae613e6ed1545f915365c405fae15998ece063db`  
		Last Modified: Wed, 10 Nov 2021 01:35:40 GMT  
		Size: 87.1 MB (87092406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35766610697c5332b1b79fc29ba7db6daa466ab9c461e0cb4b04c5fb88836940`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c55628364c58dd74d453efea996264c328e8d3ac57265dd8ca46741ace07702b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ac0020779a37b67674a9e7966eb3b53e365f1c9a9a1200a39bb6e8c9a0855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:02 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:03 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:04 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:05 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:49:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:49:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:49:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:49:39 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c71db2ec96091d918177b4caba5b8c2d89d3f78fef4eafc7ac9be00b4ec481`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28091fd75396522470a3f6501951a656411bc0380177cb74c6a86e9a10bb0457`  
		Last Modified: Wed, 10 Nov 2021 00:55:35 GMT  
		Size: 86.2 MB (86227517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9813b2cee15453f70ae9749381a1e97b8c46f9cdfa6df02d91156d46768fd0ce`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ae9fa988b63ceabfed0bdf0b7c20d9ae9606d6e93a36adc4c994849b3ea71a5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53777ed29e137e916ca6efb0b9a3f9708d5f2eb56ec8916037184765b8a58d57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:00:22 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:26 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:28 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:32 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:00:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:03:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:03:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:03:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:03:32 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:03:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253bbb84fa1eea425ed4f73f19a49bd742c24720031613e1fe123947d7fe5440`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d297f3097b64e102365b90a52a234c536ff3deb43a9c003e376b31fb2bd2`  
		Last Modified: Wed, 10 Nov 2021 03:19:20 GMT  
		Size: 91.5 MB (91540848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3794fb4895a5a92d49914af625d8427af1213db3d582df0fbdcf10c58e8b6550`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:8abb0ddefb8408d1f62553edef61756ad9e8598f475082f5f5ca89b8807b2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:978c7269e9db8dd4b1a99f6113cab668ebd7b17d44238979967d73eb8872c655
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127018178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e59bdf6f04475b9c3b17dd48dd9da27860cbba9ef57ed7c6b0b0d3d462a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 01:30:40 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 01:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:31:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:31:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:31:04 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0b425c6060ca5500da6904b6bcd19e871ed8940155c1ff657524b22c9b925`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9241e174f72407715b034a6bae613e6ed1545f915365c405fae15998ece063db`  
		Last Modified: Wed, 10 Nov 2021 01:35:40 GMT  
		Size: 87.1 MB (87092406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35766610697c5332b1b79fc29ba7db6daa466ab9c461e0cb4b04c5fb88836940`  
		Last Modified: Wed, 10 Nov 2021 01:35:27 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c55628364c58dd74d453efea996264c328e8d3ac57265dd8ca46741ace07702b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ac0020779a37b67674a9e7966eb3b53e365f1c9a9a1200a39bb6e8c9a0855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:49:02 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:03 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 00:49:04 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:05 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 00:49:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:49:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:49:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:49:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:49:38 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:49:39 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c71db2ec96091d918177b4caba5b8c2d89d3f78fef4eafc7ac9be00b4ec481`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28091fd75396522470a3f6501951a656411bc0380177cb74c6a86e9a10bb0457`  
		Last Modified: Wed, 10 Nov 2021 00:55:35 GMT  
		Size: 86.2 MB (86227517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9813b2cee15453f70ae9749381a1e97b8c46f9cdfa6df02d91156d46768fd0ce`  
		Last Modified: Wed, 10 Nov 2021 00:55:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ae9fa988b63ceabfed0bdf0b7c20d9ae9606d6e93a36adc4c994849b3ea71a5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137748879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53777ed29e137e916ca6efb0b9a3f9708d5f2eb56ec8916037184765b8a58d57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 03:00:22 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:26 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 10 Nov 2021 03:00:28 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:32 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 10 Nov 2021 03:00:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 03:00:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 03:03:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 03:03:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 03:03:22 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:03:32 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:03:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253bbb84fa1eea425ed4f73f19a49bd742c24720031613e1fe123947d7fe5440`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32d297f3097b64e102365b90a52a234c536ff3deb43a9c003e376b31fb2bd2`  
		Last Modified: Wed, 10 Nov 2021 03:19:20 GMT  
		Size: 91.5 MB (91540848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3794fb4895a5a92d49914af625d8427af1213db3d582df0fbdcf10c58e8b6550`  
		Last Modified: Wed, 10 Nov 2021 03:19:01 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:79fbd149a3dc7b18a20aa20b2c2d7e22eebdfc9326a0d1355395092b390e6a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:851139dacbbb9f342ff57850ee0dc515f659727faf5356b3b4c71077de4cae29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127719379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6599b046f3215fa337431f537c86e973bd1fbeb9baf9d8921340ad1670c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:29:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:29:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:29:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:29:59 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:29:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10058b6c45e5565e6186c65a2cc0cf93f67fdf92ac690b30a9a4f7c640c5bc3`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ac6f8b619522952b437d04ee3c5f030c88f4b086fed058e0a77c6db144f64`  
		Last Modified: Wed, 10 Nov 2021 01:34:34 GMT  
		Size: 87.8 MB (87793606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6260e28f2886e81211c3e74ee6bff4c33f7ab31c47123988ee14884e6241f9b9`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f4b6e74c2f0c70f2299759cff8fb30550b5314882542931e6e3b8c37c5a34c81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124875983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f96c151bda8d115bb261123273584d85ea3bcf689105b99c308ea5595a1081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:47:23 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:24 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:25 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:26 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:47:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:07 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134d1cd3553bd46acc1e69a24c42d9849d6b7a0ad399a083a78acfb8c0bcb74d`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bc7366474675c4e46c292a017c671244e920c31effa69d2f6d619e4a34c49e`  
		Last Modified: Wed, 10 Nov 2021 00:54:21 GMT  
		Size: 86.8 MB (86800004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff52a2f89ed856173322f636b2807b0149b0ec455d7f61d33c1f526e552095`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f8a4b6793fc07a26246d511968e9f6633be0d4a2b3c8226b0f3a4d629fb77ef4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138434268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b764d61f3c43b4dd6b14af5da376b2bd428b3f866343f86e52f0e8f08e372890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:51:24 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:27 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:30 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:34 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:51:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:54:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:54:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:54:48 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 02:55:08 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 02:55:22 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef490621d8981ee83b0dceaf9d7c7e2f4ed15972f3bab0db2a1d2a7eed83f5a`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a00561f2f6551dc642b3ce9e4dff816fe70b703acaef55790c6daaa5147fe`  
		Last Modified: Wed, 10 Nov 2021 03:17:55 GMT  
		Size: 92.2 MB (92226238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de9df0be0812cb74b4ffed1b9c4fa6e49b5c71813472410bf55ad454d01ef33`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:79fbd149a3dc7b18a20aa20b2c2d7e22eebdfc9326a0d1355395092b390e6a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:851139dacbbb9f342ff57850ee0dc515f659727faf5356b3b4c71077de4cae29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127719379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6599b046f3215fa337431f537c86e973bd1fbeb9baf9d8921340ad1670c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:29:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:29:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:29:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:29:59 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:29:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10058b6c45e5565e6186c65a2cc0cf93f67fdf92ac690b30a9a4f7c640c5bc3`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ac6f8b619522952b437d04ee3c5f030c88f4b086fed058e0a77c6db144f64`  
		Last Modified: Wed, 10 Nov 2021 01:34:34 GMT  
		Size: 87.8 MB (87793606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6260e28f2886e81211c3e74ee6bff4c33f7ab31c47123988ee14884e6241f9b9`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f4b6e74c2f0c70f2299759cff8fb30550b5314882542931e6e3b8c37c5a34c81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124875983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f96c151bda8d115bb261123273584d85ea3bcf689105b99c308ea5595a1081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:47:23 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:24 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:25 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:26 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:47:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:07 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134d1cd3553bd46acc1e69a24c42d9849d6b7a0ad399a083a78acfb8c0bcb74d`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bc7366474675c4e46c292a017c671244e920c31effa69d2f6d619e4a34c49e`  
		Last Modified: Wed, 10 Nov 2021 00:54:21 GMT  
		Size: 86.8 MB (86800004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff52a2f89ed856173322f636b2807b0149b0ec455d7f61d33c1f526e552095`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f8a4b6793fc07a26246d511968e9f6633be0d4a2b3c8226b0f3a4d629fb77ef4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138434268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b764d61f3c43b4dd6b14af5da376b2bd428b3f866343f86e52f0e8f08e372890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:51:24 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:27 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:30 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:34 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:51:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:54:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:54:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:54:48 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 02:55:08 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 02:55:22 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef490621d8981ee83b0dceaf9d7c7e2f4ed15972f3bab0db2a1d2a7eed83f5a`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a00561f2f6551dc642b3ce9e4dff816fe70b703acaef55790c6daaa5147fe`  
		Last Modified: Wed, 10 Nov 2021 03:17:55 GMT  
		Size: 92.2 MB (92226238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de9df0be0812cb74b4ffed1b9c4fa6e49b5c71813472410bf55ad454d01ef33`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:79fbd149a3dc7b18a20aa20b2c2d7e22eebdfc9326a0d1355395092b390e6a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1` - linux; amd64

```console
$ docker pull mariadb@sha256:851139dacbbb9f342ff57850ee0dc515f659727faf5356b3b4c71077de4cae29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127719379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6599b046f3215fa337431f537c86e973bd1fbeb9baf9d8921340ad1670c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:29:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:29:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:29:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:29:59 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:29:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10058b6c45e5565e6186c65a2cc0cf93f67fdf92ac690b30a9a4f7c640c5bc3`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ac6f8b619522952b437d04ee3c5f030c88f4b086fed058e0a77c6db144f64`  
		Last Modified: Wed, 10 Nov 2021 01:34:34 GMT  
		Size: 87.8 MB (87793606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6260e28f2886e81211c3e74ee6bff4c33f7ab31c47123988ee14884e6241f9b9`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f4b6e74c2f0c70f2299759cff8fb30550b5314882542931e6e3b8c37c5a34c81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124875983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f96c151bda8d115bb261123273584d85ea3bcf689105b99c308ea5595a1081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:47:23 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:24 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:25 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:26 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:47:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:07 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134d1cd3553bd46acc1e69a24c42d9849d6b7a0ad399a083a78acfb8c0bcb74d`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bc7366474675c4e46c292a017c671244e920c31effa69d2f6d619e4a34c49e`  
		Last Modified: Wed, 10 Nov 2021 00:54:21 GMT  
		Size: 86.8 MB (86800004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff52a2f89ed856173322f636b2807b0149b0ec455d7f61d33c1f526e552095`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f8a4b6793fc07a26246d511968e9f6633be0d4a2b3c8226b0f3a4d629fb77ef4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138434268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b764d61f3c43b4dd6b14af5da376b2bd428b3f866343f86e52f0e8f08e372890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:51:24 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:27 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:30 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:34 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:51:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:54:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:54:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:54:48 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 02:55:08 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 02:55:22 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef490621d8981ee83b0dceaf9d7c7e2f4ed15972f3bab0db2a1d2a7eed83f5a`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a00561f2f6551dc642b3ce9e4dff816fe70b703acaef55790c6daaa5147fe`  
		Last Modified: Wed, 10 Nov 2021 03:17:55 GMT  
		Size: 92.2 MB (92226238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de9df0be0812cb74b4ffed1b9c4fa6e49b5c71813472410bf55ad454d01ef33`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:79fbd149a3dc7b18a20aa20b2c2d7e22eebdfc9326a0d1355395092b390e6a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:851139dacbbb9f342ff57850ee0dc515f659727faf5356b3b4c71077de4cae29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127719379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6599b046f3215fa337431f537c86e973bd1fbeb9baf9d8921340ad1670c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 01:29:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 01:29:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:29:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:29:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:29:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:29:59 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:29:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10058b6c45e5565e6186c65a2cc0cf93f67fdf92ac690b30a9a4f7c640c5bc3`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ac6f8b619522952b437d04ee3c5f030c88f4b086fed058e0a77c6db144f64`  
		Last Modified: Wed, 10 Nov 2021 01:34:34 GMT  
		Size: 87.8 MB (87793606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6260e28f2886e81211c3e74ee6bff4c33f7ab31c47123988ee14884e6241f9b9`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f4b6e74c2f0c70f2299759cff8fb30550b5314882542931e6e3b8c37c5a34c81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124875983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f96c151bda8d115bb261123273584d85ea3bcf689105b99c308ea5595a1081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:47:23 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:24 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 00:47:25 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:26 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 00:47:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:47:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:06 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:07 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134d1cd3553bd46acc1e69a24c42d9849d6b7a0ad399a083a78acfb8c0bcb74d`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bc7366474675c4e46c292a017c671244e920c31effa69d2f6d619e4a34c49e`  
		Last Modified: Wed, 10 Nov 2021 00:54:21 GMT  
		Size: 86.8 MB (86800004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff52a2f89ed856173322f636b2807b0149b0ec455d7f61d33c1f526e552095`  
		Last Modified: Wed, 10 Nov 2021 00:54:07 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f8a4b6793fc07a26246d511968e9f6633be0d4a2b3c8226b0f3a4d629fb77ef4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138434268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b764d61f3c43b4dd6b14af5da376b2bd428b3f866343f86e52f0e8f08e372890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:51:24 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:27 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 10 Nov 2021 02:51:30 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:34 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 10 Nov 2021 02:51:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:51:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:54:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:54:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:54:48 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 02:55:08 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 02:55:22 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef490621d8981ee83b0dceaf9d7c7e2f4ed15972f3bab0db2a1d2a7eed83f5a`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a00561f2f6551dc642b3ce9e4dff816fe70b703acaef55790c6daaa5147fe`  
		Last Modified: Wed, 10 Nov 2021 03:17:55 GMT  
		Size: 92.2 MB (92226238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de9df0be0812cb74b4ffed1b9c4fa6e49b5c71813472410bf55ad454d01ef33`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 5.6 KB (5626 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
$ docker pull mariadb@sha256:25487743adf754ef7b991bc0ed744087f4d135cfdab09a6f58cc3d6404100a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:528cfe83d93caba437e75039b606a4637dd5c724c6a25d7c7b64ec2e9eb11303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127209686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2278f24ac88b82f98ef58de4bf15c0b01df3de2f1fe835e2ea4350282d58700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:07:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:07:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:28:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 01:28:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 01:28:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 01:29:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 01:29:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 01:29:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 01:30:11 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 01:30:12 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 01:30:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 01:30:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 01:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 01:30:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 01:30:36 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 01:30:36 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 01:30:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034655750c88e076cbd516354371b6176d01179bf595d928444e663ba1fa6845`  
		Last Modified: Sat, 16 Oct 2021 03:11:19 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b757a2a0f02848b1254cbd8b54e1d3cd4651228ede9a8c75e127f91cb415c4`  
		Last Modified: Sat, 16 Oct 2021 03:11:20 GMT  
		Size: 5.5 MB (5489306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcce26bc5e3db198df58fab2d65d24301379f9a5b3bbff37b503df43120e93`  
		Last Modified: Wed, 10 Nov 2021 01:34:24 GMT  
		Size: 3.6 MB (3585273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f220ee926647d1f8e0052287bdaeea7f633d7101dfd961d7353f26c98babff`  
		Last Modified: Wed, 10 Nov 2021 01:34:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c8a77f78429697389a71444eed47826a59f54f8e99f94f1f31553a01901733`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.3 MB (2273746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de5652303b4dd7c45853fd8186b06583c8692fb9b76fab0d077e85f1183f19`  
		Last Modified: Wed, 10 Nov 2021 01:34:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef669123e59e21dfcfb135d17b7cf2c63010103cdf9f94dba9b61bc7b86dc43a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cec468d3a69f2df00e672e7749369fd082ab7a9c54953c20e3594d65a3c7aa`  
		Last Modified: Wed, 10 Nov 2021 01:35:02 GMT  
		Size: 87.3 MB (87283911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1ba1d651dce9d9e1048dcd199b38b8aff40b0769e0e347f3b7ad8179619a`  
		Last Modified: Wed, 10 Nov 2021 01:34:49 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1b55db5e372df82c3ae7585218449011fff5a17ad93b6b4fe1ecc11a56b99114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124382638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda4c38372fd9df7ce63b79880638b8bd52077a453c28a38c8cb0c96a26bd26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:45:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 03:45:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:46:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 00:47:05 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 00:47:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 00:47:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 00:47:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 00:47:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 00:48:15 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:16 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 00:48:17 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:18 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 00:48:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 00:48:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 00:48:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 00:48:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 00:48:52 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 00:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 00:48:53 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 00:48:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c05479159a3de34e1aedf676cd1a6793673b2e223d06a85c1caeab97e08c15`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3fae4be7ce6b0048b0994bc5bd1e2d202fb383de08c3f2b82896678b35e8d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:12 GMT  
		Size: 5.3 MB (5320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f314de44c1d87f106753ca38adfd4ac0d2ce3c3cd6c7c2ec9d3d26a4eb4ad3`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 3.4 MB (3370347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a2529e55ed4f037d168f1dd29071054607aa460f9285cc780ce26402e1f9c5`  
		Last Modified: Wed, 10 Nov 2021 00:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e027baf10a6a81ff40d26819c900ce7532be4894aaf3591b05d5325ae5bc2fc`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.2 MB (2203685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba14cc653d82df49ba5a8866a1aa2e53de87cff7eaf2d439f77c0488cbe5975`  
		Last Modified: Wed, 10 Nov 2021 00:54:08 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ef25d84c30123544a560174c4d5cf5a6b194d74c43c6e0ce41f7c124a6eaf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed92b0fe892e9a983f98c592c8d4c580816be2395b610966a02f76c3a4f595`  
		Last Modified: Wed, 10 Nov 2021 00:54:52 GMT  
		Size: 86.3 MB (86306663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22a51b43003d4dd5a40af8103acabf5f2f665c6f724f1969befcea9abd94bf`  
		Last Modified: Wed, 10 Nov 2021 00:54:38 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:185ecaa4696da252c45a687b868c17a657bfc4de463a39e4b039461073c8b2b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27901b4c7fadea579efbd0e8f5e70acfdaa96cde1e390040d8734c3f41809d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:34:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 16 Oct 2021 01:34:51 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:48:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 10 Nov 2021 02:50:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 10 Nov 2021 02:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Nov 2021 02:51:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 02:51:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 10 Nov 2021 02:51:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 10 Nov 2021 02:55:37 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:41 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 10 Nov 2021 02:55:43 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:47 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 10 Nov 2021 02:55:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 10 Nov 2021 02:56:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 10 Nov 2021 02:59:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 10 Nov 2021 02:59:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 10 Nov 2021 02:59:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 10 Nov 2021 03:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Nov 2021 03:00:05 GMT
EXPOSE 3306
# Wed, 10 Nov 2021 03:00:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9c5581eb228ed7e984fa7a4e62a7f8b2a068039fde3d32fa3b208026a189d`  
		Last Modified: Sat, 16 Oct 2021 01:49:31 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d968d5ad046645779be85243a3db326487bc8905dabf68bb063ea79e1662c1`  
		Last Modified: Sat, 16 Oct 2021 01:49:32 GMT  
		Size: 6.7 MB (6667970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338074e1d5ab45535164f793f5cd39346c448764012b0242e0dbcffbfeed958`  
		Last Modified: Wed, 10 Nov 2021 03:17:41 GMT  
		Size: 3.7 MB (3673084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40418ec2a5f7b4d685948c6a3fd03d6d1b8dfa933c0c74dccd9367c63192e58`  
		Last Modified: Wed, 10 Nov 2021 03:17:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913fb2cbb2af8690d3b6a461bfc9e7792eec167f5bca73d3e682a54d6b3094b`  
		Last Modified: Wed, 10 Nov 2021 03:17:37 GMT  
		Size: 2.6 MB (2569382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ebc19f9b2fd40781356cda8639723d7c63414cf30b7b328e2a56558d504b3`  
		Last Modified: Wed, 10 Nov 2021 03:17:36 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005785a8c2f750f37cf9239804468b179b88e16bd90ca1e41b16d6463b9c23`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a85797dd5c660cffd18794aea89f13e93f226ac71697399cb94d72747d931`  
		Last Modified: Wed, 10 Nov 2021 03:18:31 GMT  
		Size: 91.6 MB (91575664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76466bb67a50543931e108563c01fb06676eba38e3aa36022373131e38a38a28`  
		Last Modified: Wed, 10 Nov 2021 03:18:12 GMT  
		Size: 5.6 KB (5625 bytes)  
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
