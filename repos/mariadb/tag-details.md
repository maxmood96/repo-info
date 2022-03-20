<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.43`](#mariadb10243)
-	[`mariadb:10.2.43-bionic`](#mariadb10243-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.34`](#mariadb10334)
-	[`mariadb:10.3.34-focal`](#mariadb10334-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.24`](#mariadb10424)
-	[`mariadb:10.4.24-focal`](#mariadb10424-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.15`](#mariadb10515)
-	[`mariadb:10.5.15-focal`](#mariadb10515-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.7`](#mariadb1067)
-	[`mariadb:10.6.7-focal`](#mariadb1067-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.3`](#mariadb1073)
-	[`mariadb:10.7.3-focal`](#mariadb1073-focal)
-	[`mariadb:10.8-rc`](#mariadb108-rc)
-	[`mariadb:10.8-rc-focal`](#mariadb108-rc-focal)
-	[`mariadb:10.8.2-rc`](#mariadb1082-rc)
-	[`mariadb:10.8.2-rc-focal`](#mariadb1082-rc-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:efd46a418f4d2e0e5bcb2ae9cf70e5f6f6506f44150fe05dba5f67bffa960ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:bc91639a97d7999882aa5f6a435e259a3df7ee3e3e77b74919fdb90d07f971cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f59fef3784ee949a07c358d3c79b505df4eb68c726c77671b2ebe823b64387c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:45:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:45:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:25 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:45:40 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:45:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:45:50 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:46:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 17:46:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:47:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:47:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:47:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:47:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a91d1249fbbfd5eabe0cc502ba4c3a1c42e90f7a1c5024baa31fbee3245eaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe6b683d09debe024ce8233f165cf67c020731e1a9453e88a2abfc48a3cfaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 4.8 MB (4813120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e29130a2f27ed17a5f6fdd8e4ea7bbffad70c053614b83a299550c06580ad5`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 3.6 MB (3553133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272d2871b3b4e171df7e526ea193d9a53607a580898f98de091f7c8a7eeaa499`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60a60f55b37f8c95a0cf7174d794349b78204b623d3a49c325d2b2528748a6`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 1.6 MB (1583562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f8e43cbeb61f8ee761c3f7d7788461a2f155664cac0637e006c6d72161619`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf46223049f572ebd4ff3e9e9f95aceca06ad68479366d66a44fedd458c30c7`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8f2f3395605407074810498326f8da5b360c036c1c4568bdfcb6b3a1222d3c`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 72.6 MB (72639635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b64df62d53ea6c60d621c2532e4cbad0d92abb591017c0ceb3ba11a106ab27`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6dedf408d55fbc3445565cd16acc9315fd9baa1bed230c8f6d34a17e7c688f`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46521e37069739bddf5c1d700b96cce4fc0631ba7c4d7053065190612701cd2a`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:cd23bc3563b8fb31c0d6235109327dd4e47577ef2389d2ac93e16c3323e78feb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104250740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d832f5e939541cabe04d302be07a783fec73c00478f70978c2e7c7cb2df3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:52:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:52:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:29 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:52:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:52:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:53:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:53:38 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:39 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:40 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:41 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 15:53:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:54:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:54:12 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:54:13 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:54:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:54:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6f994bfbf33556557870d680bfb59a17e52c2e38a7d1ce724b992dd23eeb75`  
		Last Modified: Sat, 19 Mar 2022 15:58:57 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382b1c8a1df2b650d8dc944d39e9c4731aa1a06762046579fbefcb3bef8ca3a`  
		Last Modified: Sat, 19 Mar 2022 15:58:58 GMT  
		Size: 4.3 MB (4261595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad3def2abaae58f31858d82d8b45090e238115c7423b82f3ddda99a248f397`  
		Last Modified: Sat, 19 Mar 2022 15:58:56 GMT  
		Size: 3.2 MB (3207358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58ef3378b636b74d53b76a046991039603b39a47a9f9fed8ab1505794724b94`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c9ba462c569efb2b750f55d33f1bbbb673235eb0939b7ceb694cb76175bf9`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 1.5 MB (1529531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e881343a5c49523191bfa9b10ff7effb126aa90d9a5a530366507bf94f4db5c3`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83475f324edbd6da0f115c59a5a06c74398d02c0812ad087703af6a174062b65`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d505396c3475c0c82ce6b36ba7ef4df88f3fa8168145a5526c68c64f33d84d`  
		Last Modified: Sat, 19 Mar 2022 15:59:04 GMT  
		Size: 71.5 MB (71505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d95d7dfffbb0b7360bde616a8a6377a31b51347eeb08f00792507657d7732`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb37d55098f3c2ba4baae8c3e4717e6f0bcc218de5360f9483e22006553fef6`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2624a99bc3e80cb7905f2f5d8e7e0757853590e00ed7b9987e71f367e223600`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e53476cc53b2f777384b29c75007024169e98756b24ae2ff1ab95bcf2e0955dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727fcfc3afab8cc7f918db91c5ed9603f83bca32a3a30e83ce46f158ea4234f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:23:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:23:54 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:23:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9085873a4e749126d12ced9b2fd7a924740fa69617754cf0a8b1110a31b2938`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a9022751c2d17a8fdc528ce5112777ee73b468f77fa9dbc0ca805b8bf66cc`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:efd46a418f4d2e0e5bcb2ae9cf70e5f6f6506f44150fe05dba5f67bffa960ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bc91639a97d7999882aa5f6a435e259a3df7ee3e3e77b74919fdb90d07f971cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f59fef3784ee949a07c358d3c79b505df4eb68c726c77671b2ebe823b64387c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:45:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:45:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:25 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:45:40 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:45:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:45:50 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:46:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 17:46:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:47:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:47:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:47:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:47:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a91d1249fbbfd5eabe0cc502ba4c3a1c42e90f7a1c5024baa31fbee3245eaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe6b683d09debe024ce8233f165cf67c020731e1a9453e88a2abfc48a3cfaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 4.8 MB (4813120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e29130a2f27ed17a5f6fdd8e4ea7bbffad70c053614b83a299550c06580ad5`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 3.6 MB (3553133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272d2871b3b4e171df7e526ea193d9a53607a580898f98de091f7c8a7eeaa499`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60a60f55b37f8c95a0cf7174d794349b78204b623d3a49c325d2b2528748a6`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 1.6 MB (1583562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f8e43cbeb61f8ee761c3f7d7788461a2f155664cac0637e006c6d72161619`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf46223049f572ebd4ff3e9e9f95aceca06ad68479366d66a44fedd458c30c7`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8f2f3395605407074810498326f8da5b360c036c1c4568bdfcb6b3a1222d3c`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 72.6 MB (72639635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b64df62d53ea6c60d621c2532e4cbad0d92abb591017c0ceb3ba11a106ab27`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6dedf408d55fbc3445565cd16acc9315fd9baa1bed230c8f6d34a17e7c688f`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46521e37069739bddf5c1d700b96cce4fc0631ba7c4d7053065190612701cd2a`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:cd23bc3563b8fb31c0d6235109327dd4e47577ef2389d2ac93e16c3323e78feb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104250740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d832f5e939541cabe04d302be07a783fec73c00478f70978c2e7c7cb2df3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:52:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:52:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:29 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:52:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:52:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:53:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:53:38 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:39 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:40 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:41 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 15:53:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:54:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:54:12 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:54:13 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:54:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:54:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6f994bfbf33556557870d680bfb59a17e52c2e38a7d1ce724b992dd23eeb75`  
		Last Modified: Sat, 19 Mar 2022 15:58:57 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382b1c8a1df2b650d8dc944d39e9c4731aa1a06762046579fbefcb3bef8ca3a`  
		Last Modified: Sat, 19 Mar 2022 15:58:58 GMT  
		Size: 4.3 MB (4261595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad3def2abaae58f31858d82d8b45090e238115c7423b82f3ddda99a248f397`  
		Last Modified: Sat, 19 Mar 2022 15:58:56 GMT  
		Size: 3.2 MB (3207358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58ef3378b636b74d53b76a046991039603b39a47a9f9fed8ab1505794724b94`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c9ba462c569efb2b750f55d33f1bbbb673235eb0939b7ceb694cb76175bf9`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 1.5 MB (1529531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e881343a5c49523191bfa9b10ff7effb126aa90d9a5a530366507bf94f4db5c3`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83475f324edbd6da0f115c59a5a06c74398d02c0812ad087703af6a174062b65`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d505396c3475c0c82ce6b36ba7ef4df88f3fa8168145a5526c68c64f33d84d`  
		Last Modified: Sat, 19 Mar 2022 15:59:04 GMT  
		Size: 71.5 MB (71505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d95d7dfffbb0b7360bde616a8a6377a31b51347eeb08f00792507657d7732`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb37d55098f3c2ba4baae8c3e4717e6f0bcc218de5360f9483e22006553fef6`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2624a99bc3e80cb7905f2f5d8e7e0757853590e00ed7b9987e71f367e223600`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e53476cc53b2f777384b29c75007024169e98756b24ae2ff1ab95bcf2e0955dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727fcfc3afab8cc7f918db91c5ed9603f83bca32a3a30e83ce46f158ea4234f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:23:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:23:54 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:23:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9085873a4e749126d12ced9b2fd7a924740fa69617754cf0a8b1110a31b2938`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a9022751c2d17a8fdc528ce5112777ee73b468f77fa9dbc0ca805b8bf66cc`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43`

```console
$ docker pull mariadb@sha256:efd46a418f4d2e0e5bcb2ae9cf70e5f6f6506f44150fe05dba5f67bffa960ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43` - linux; amd64

```console
$ docker pull mariadb@sha256:bc91639a97d7999882aa5f6a435e259a3df7ee3e3e77b74919fdb90d07f971cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f59fef3784ee949a07c358d3c79b505df4eb68c726c77671b2ebe823b64387c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:45:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:45:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:25 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:45:40 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:45:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:45:50 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:46:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 17:46:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:47:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:47:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:47:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:47:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a91d1249fbbfd5eabe0cc502ba4c3a1c42e90f7a1c5024baa31fbee3245eaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe6b683d09debe024ce8233f165cf67c020731e1a9453e88a2abfc48a3cfaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 4.8 MB (4813120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e29130a2f27ed17a5f6fdd8e4ea7bbffad70c053614b83a299550c06580ad5`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 3.6 MB (3553133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272d2871b3b4e171df7e526ea193d9a53607a580898f98de091f7c8a7eeaa499`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60a60f55b37f8c95a0cf7174d794349b78204b623d3a49c325d2b2528748a6`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 1.6 MB (1583562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f8e43cbeb61f8ee761c3f7d7788461a2f155664cac0637e006c6d72161619`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf46223049f572ebd4ff3e9e9f95aceca06ad68479366d66a44fedd458c30c7`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8f2f3395605407074810498326f8da5b360c036c1c4568bdfcb6b3a1222d3c`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 72.6 MB (72639635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b64df62d53ea6c60d621c2532e4cbad0d92abb591017c0ceb3ba11a106ab27`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6dedf408d55fbc3445565cd16acc9315fd9baa1bed230c8f6d34a17e7c688f`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46521e37069739bddf5c1d700b96cce4fc0631ba7c4d7053065190612701cd2a`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:cd23bc3563b8fb31c0d6235109327dd4e47577ef2389d2ac93e16c3323e78feb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104250740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d832f5e939541cabe04d302be07a783fec73c00478f70978c2e7c7cb2df3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:52:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:52:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:29 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:52:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:52:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:53:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:53:38 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:39 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:40 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:41 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 15:53:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:54:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:54:12 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:54:13 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:54:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:54:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6f994bfbf33556557870d680bfb59a17e52c2e38a7d1ce724b992dd23eeb75`  
		Last Modified: Sat, 19 Mar 2022 15:58:57 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382b1c8a1df2b650d8dc944d39e9c4731aa1a06762046579fbefcb3bef8ca3a`  
		Last Modified: Sat, 19 Mar 2022 15:58:58 GMT  
		Size: 4.3 MB (4261595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad3def2abaae58f31858d82d8b45090e238115c7423b82f3ddda99a248f397`  
		Last Modified: Sat, 19 Mar 2022 15:58:56 GMT  
		Size: 3.2 MB (3207358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58ef3378b636b74d53b76a046991039603b39a47a9f9fed8ab1505794724b94`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c9ba462c569efb2b750f55d33f1bbbb673235eb0939b7ceb694cb76175bf9`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 1.5 MB (1529531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e881343a5c49523191bfa9b10ff7effb126aa90d9a5a530366507bf94f4db5c3`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83475f324edbd6da0f115c59a5a06c74398d02c0812ad087703af6a174062b65`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d505396c3475c0c82ce6b36ba7ef4df88f3fa8168145a5526c68c64f33d84d`  
		Last Modified: Sat, 19 Mar 2022 15:59:04 GMT  
		Size: 71.5 MB (71505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d95d7dfffbb0b7360bde616a8a6377a31b51347eeb08f00792507657d7732`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb37d55098f3c2ba4baae8c3e4717e6f0bcc218de5360f9483e22006553fef6`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2624a99bc3e80cb7905f2f5d8e7e0757853590e00ed7b9987e71f367e223600`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e53476cc53b2f777384b29c75007024169e98756b24ae2ff1ab95bcf2e0955dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727fcfc3afab8cc7f918db91c5ed9603f83bca32a3a30e83ce46f158ea4234f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:23:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:23:54 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:23:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9085873a4e749126d12ced9b2fd7a924740fa69617754cf0a8b1110a31b2938`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a9022751c2d17a8fdc528ce5112777ee73b468f77fa9dbc0ca805b8bf66cc`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43-bionic`

```console
$ docker pull mariadb@sha256:efd46a418f4d2e0e5bcb2ae9cf70e5f6f6506f44150fe05dba5f67bffa960ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bc91639a97d7999882aa5f6a435e259a3df7ee3e3e77b74919fdb90d07f971cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f59fef3784ee949a07c358d3c79b505df4eb68c726c77671b2ebe823b64387c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:45:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:45:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:25 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:45:40 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:45:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:45:50 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:45:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:46:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 17:46:26 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:26 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 17:46:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 17:46:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:47:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:47:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:47:06 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:47:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:47:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a91d1249fbbfd5eabe0cc502ba4c3a1c42e90f7a1c5024baa31fbee3245eaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe6b683d09debe024ce8233f165cf67c020731e1a9453e88a2abfc48a3cfaf`  
		Last Modified: Sat, 19 Mar 2022 17:51:09 GMT  
		Size: 4.8 MB (4813120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e29130a2f27ed17a5f6fdd8e4ea7bbffad70c053614b83a299550c06580ad5`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 3.6 MB (3553133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272d2871b3b4e171df7e526ea193d9a53607a580898f98de091f7c8a7eeaa499`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60a60f55b37f8c95a0cf7174d794349b78204b623d3a49c325d2b2528748a6`  
		Last Modified: Sat, 19 Mar 2022 17:51:07 GMT  
		Size: 1.6 MB (1583562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f8e43cbeb61f8ee761c3f7d7788461a2f155664cac0637e006c6d72161619`  
		Last Modified: Sat, 19 Mar 2022 17:51:06 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf46223049f572ebd4ff3e9e9f95aceca06ad68479366d66a44fedd458c30c7`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8f2f3395605407074810498326f8da5b360c036c1c4568bdfcb6b3a1222d3c`  
		Last Modified: Sat, 19 Mar 2022 17:51:16 GMT  
		Size: 72.6 MB (72639635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b64df62d53ea6c60d621c2532e4cbad0d92abb591017c0ceb3ba11a106ab27`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6dedf408d55fbc3445565cd16acc9315fd9baa1bed230c8f6d34a17e7c688f`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46521e37069739bddf5c1d700b96cce4fc0631ba7c4d7053065190612701cd2a`  
		Last Modified: Sat, 19 Mar 2022 17:51:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:cd23bc3563b8fb31c0d6235109327dd4e47577ef2389d2ac93e16c3323e78feb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104250740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d832f5e939541cabe04d302be07a783fec73c00478f70978c2e7c7cb2df3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:52:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:52:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:29 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:52:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:52:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:52:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:53:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:53:38 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:39 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 15:53:40 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:41 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 15:53:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 15:53:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:54:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:54:12 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:54:13 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:54:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:54:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6f994bfbf33556557870d680bfb59a17e52c2e38a7d1ce724b992dd23eeb75`  
		Last Modified: Sat, 19 Mar 2022 15:58:57 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382b1c8a1df2b650d8dc944d39e9c4731aa1a06762046579fbefcb3bef8ca3a`  
		Last Modified: Sat, 19 Mar 2022 15:58:58 GMT  
		Size: 4.3 MB (4261595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad3def2abaae58f31858d82d8b45090e238115c7423b82f3ddda99a248f397`  
		Last Modified: Sat, 19 Mar 2022 15:58:56 GMT  
		Size: 3.2 MB (3207358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58ef3378b636b74d53b76a046991039603b39a47a9f9fed8ab1505794724b94`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c9ba462c569efb2b750f55d33f1bbbb673235eb0939b7ceb694cb76175bf9`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 1.5 MB (1529531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e881343a5c49523191bfa9b10ff7effb126aa90d9a5a530366507bf94f4db5c3`  
		Last Modified: Sat, 19 Mar 2022 15:58:55 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83475f324edbd6da0f115c59a5a06c74398d02c0812ad087703af6a174062b65`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d505396c3475c0c82ce6b36ba7ef4df88f3fa8168145a5526c68c64f33d84d`  
		Last Modified: Sat, 19 Mar 2022 15:59:04 GMT  
		Size: 71.5 MB (71505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d95d7dfffbb0b7360bde616a8a6377a31b51347eeb08f00792507657d7732`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb37d55098f3c2ba4baae8c3e4717e6f0bcc218de5360f9483e22006553fef6`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2624a99bc3e80cb7905f2f5d8e7e0757853590e00ed7b9987e71f367e223600`  
		Last Modified: Sat, 19 Mar 2022 15:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e53476cc53b2f777384b29c75007024169e98756b24ae2ff1ab95bcf2e0955dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727fcfc3afab8cc7f918db91c5ed9603f83bca32a3a30e83ce46f158ea4234f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:23:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:23:54 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:23:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9085873a4e749126d12ced9b2fd7a924740fa69617754cf0a8b1110a31b2938`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a9022751c2d17a8fdc528ce5112777ee73b468f77fa9dbc0ca805b8bf66cc`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:0179b5bc3f603412021d29f667f13a949ae78282d9e750ba21af67dddce9a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:a02950f72b1c11d4456420674c0c786b93653db701d7044dec743024c39cb884
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120118593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f42216767ea946a7c1bdca6d1845bf583984585cedbe687c691a4f4c51c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:44:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567a71d6c3c00a0e8c4010a6515de5006de9fb555d8e8ccd4329e31ad88cb0c`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3638db20ec31d2a1ca86600df74b067adbba4a85d59290a02fe7c06512538`  
		Last Modified: Sat, 19 Mar 2022 17:50:48 GMT  
		Size: 80.2 MB (80191076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5892ef5a3b86041a21780ba0f7c9e64e3809183a6eada019ef67133485a23c8`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f663a1410ad3ecbba49d178250d1072e5f301e736c39c4a478492e2618f3324`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297a4218cdc781c24b4fe7263b6c48ecca58e08ecd2675f0f9e3f3e7a7db132`  
		Last Modified: Sat, 19 Mar 2022 17:50:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4469a09803b91bee0060aa1780eb0f35ea2f7fb53e2876adf67d44ae8528e307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1630d07b0c464a56976cdd9baaa19087d487e7c55805630f993acdca940c409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:51:33 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:33 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:34 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:35 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:51:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:52:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:52:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:52:04 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:52:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:52:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:52:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:52:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7be4221622947ae699e2ef73931c9ea9a48eda7f0ba5908c0e3d05456633123`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed63f4d89994154bab2bb119734d3582407dbfa6049ef49819eacbdb4633df0`  
		Last Modified: Sat, 19 Mar 2022 15:58:33 GMT  
		Size: 79.5 MB (79531244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69271f12126c31cd926d6a90296d4624e8d99cd4217be0c60a0ef27c4f2381ee`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772457a33822e992596fbbca1a3e4a9900bca6de57d11b2a25cf9bc5b65a2b4a`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c33bd6c406a7c730d88f4b2051bf47d1746add2061ec74ee61488da52f7e0`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f91098fa46f3f8074dba47e4669bb256bfa7ea3ebeb5a4d52edc0e71b5993f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1331873d894a0f7eddf55636db7705a2703669e70d4555e1b131c86a130eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:18:25 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:18:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:18:35 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932fc72603790eed7a6544b8dbb7d9bb03fb889e881905748edd17ea7cc6dde`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4ee59423c4bad6b210d80822104f021daf7fe0244dba656ed9b81fa84efc7`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:0179b5bc3f603412021d29f667f13a949ae78282d9e750ba21af67dddce9a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a02950f72b1c11d4456420674c0c786b93653db701d7044dec743024c39cb884
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120118593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f42216767ea946a7c1bdca6d1845bf583984585cedbe687c691a4f4c51c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:44:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567a71d6c3c00a0e8c4010a6515de5006de9fb555d8e8ccd4329e31ad88cb0c`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3638db20ec31d2a1ca86600df74b067adbba4a85d59290a02fe7c06512538`  
		Last Modified: Sat, 19 Mar 2022 17:50:48 GMT  
		Size: 80.2 MB (80191076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5892ef5a3b86041a21780ba0f7c9e64e3809183a6eada019ef67133485a23c8`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f663a1410ad3ecbba49d178250d1072e5f301e736c39c4a478492e2618f3324`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297a4218cdc781c24b4fe7263b6c48ecca58e08ecd2675f0f9e3f3e7a7db132`  
		Last Modified: Sat, 19 Mar 2022 17:50:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4469a09803b91bee0060aa1780eb0f35ea2f7fb53e2876adf67d44ae8528e307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1630d07b0c464a56976cdd9baaa19087d487e7c55805630f993acdca940c409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:51:33 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:33 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:34 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:35 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:51:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:52:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:52:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:52:04 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:52:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:52:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:52:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:52:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7be4221622947ae699e2ef73931c9ea9a48eda7f0ba5908c0e3d05456633123`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed63f4d89994154bab2bb119734d3582407dbfa6049ef49819eacbdb4633df0`  
		Last Modified: Sat, 19 Mar 2022 15:58:33 GMT  
		Size: 79.5 MB (79531244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69271f12126c31cd926d6a90296d4624e8d99cd4217be0c60a0ef27c4f2381ee`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772457a33822e992596fbbca1a3e4a9900bca6de57d11b2a25cf9bc5b65a2b4a`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c33bd6c406a7c730d88f4b2051bf47d1746add2061ec74ee61488da52f7e0`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f91098fa46f3f8074dba47e4669bb256bfa7ea3ebeb5a4d52edc0e71b5993f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1331873d894a0f7eddf55636db7705a2703669e70d4555e1b131c86a130eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:18:25 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:18:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:18:35 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932fc72603790eed7a6544b8dbb7d9bb03fb889e881905748edd17ea7cc6dde`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4ee59423c4bad6b210d80822104f021daf7fe0244dba656ed9b81fa84efc7`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34`

```console
$ docker pull mariadb@sha256:0179b5bc3f603412021d29f667f13a949ae78282d9e750ba21af67dddce9a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34` - linux; amd64

```console
$ docker pull mariadb@sha256:a02950f72b1c11d4456420674c0c786b93653db701d7044dec743024c39cb884
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120118593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f42216767ea946a7c1bdca6d1845bf583984585cedbe687c691a4f4c51c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:44:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567a71d6c3c00a0e8c4010a6515de5006de9fb555d8e8ccd4329e31ad88cb0c`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3638db20ec31d2a1ca86600df74b067adbba4a85d59290a02fe7c06512538`  
		Last Modified: Sat, 19 Mar 2022 17:50:48 GMT  
		Size: 80.2 MB (80191076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5892ef5a3b86041a21780ba0f7c9e64e3809183a6eada019ef67133485a23c8`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f663a1410ad3ecbba49d178250d1072e5f301e736c39c4a478492e2618f3324`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297a4218cdc781c24b4fe7263b6c48ecca58e08ecd2675f0f9e3f3e7a7db132`  
		Last Modified: Sat, 19 Mar 2022 17:50:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4469a09803b91bee0060aa1780eb0f35ea2f7fb53e2876adf67d44ae8528e307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1630d07b0c464a56976cdd9baaa19087d487e7c55805630f993acdca940c409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:51:33 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:33 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:34 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:35 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:51:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:52:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:52:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:52:04 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:52:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:52:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:52:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:52:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7be4221622947ae699e2ef73931c9ea9a48eda7f0ba5908c0e3d05456633123`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed63f4d89994154bab2bb119734d3582407dbfa6049ef49819eacbdb4633df0`  
		Last Modified: Sat, 19 Mar 2022 15:58:33 GMT  
		Size: 79.5 MB (79531244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69271f12126c31cd926d6a90296d4624e8d99cd4217be0c60a0ef27c4f2381ee`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772457a33822e992596fbbca1a3e4a9900bca6de57d11b2a25cf9bc5b65a2b4a`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c33bd6c406a7c730d88f4b2051bf47d1746add2061ec74ee61488da52f7e0`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f91098fa46f3f8074dba47e4669bb256bfa7ea3ebeb5a4d52edc0e71b5993f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1331873d894a0f7eddf55636db7705a2703669e70d4555e1b131c86a130eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:18:25 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:18:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:18:35 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932fc72603790eed7a6544b8dbb7d9bb03fb889e881905748edd17ea7cc6dde`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4ee59423c4bad6b210d80822104f021daf7fe0244dba656ed9b81fa84efc7`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34-focal`

```console
$ docker pull mariadb@sha256:0179b5bc3f603412021d29f667f13a949ae78282d9e750ba21af67dddce9a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:a02950f72b1c11d4456420674c0c786b93653db701d7044dec743024c39cb884
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120118593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f42216767ea946a7c1bdca6d1845bf583984585cedbe687c691a4f4c51c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 17:44:27 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 17:44:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:44:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:55 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567a71d6c3c00a0e8c4010a6515de5006de9fb555d8e8ccd4329e31ad88cb0c`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3638db20ec31d2a1ca86600df74b067adbba4a85d59290a02fe7c06512538`  
		Last Modified: Sat, 19 Mar 2022 17:50:48 GMT  
		Size: 80.2 MB (80191076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5892ef5a3b86041a21780ba0f7c9e64e3809183a6eada019ef67133485a23c8`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f663a1410ad3ecbba49d178250d1072e5f301e736c39c4a478492e2618f3324`  
		Last Modified: Sat, 19 Mar 2022 17:50:35 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297a4218cdc781c24b4fe7263b6c48ecca58e08ecd2675f0f9e3f3e7a7db132`  
		Last Modified: Sat, 19 Mar 2022 17:50:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4469a09803b91bee0060aa1780eb0f35ea2f7fb53e2876adf67d44ae8528e307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1630d07b0c464a56976cdd9baaa19087d487e7c55805630f993acdca940c409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:51:33 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:33 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 15:51:34 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:35 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 15:51:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:51:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:52:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:52:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:52:04 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:52:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:52:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:52:07 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:52:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7be4221622947ae699e2ef73931c9ea9a48eda7f0ba5908c0e3d05456633123`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed63f4d89994154bab2bb119734d3582407dbfa6049ef49819eacbdb4633df0`  
		Last Modified: Sat, 19 Mar 2022 15:58:33 GMT  
		Size: 79.5 MB (79531244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69271f12126c31cd926d6a90296d4624e8d99cd4217be0c60a0ef27c4f2381ee`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772457a33822e992596fbbca1a3e4a9900bca6de57d11b2a25cf9bc5b65a2b4a`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c33bd6c406a7c730d88f4b2051bf47d1746add2061ec74ee61488da52f7e0`  
		Last Modified: Sat, 19 Mar 2022 15:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f91098fa46f3f8074dba47e4669bb256bfa7ea3ebeb5a4d52edc0e71b5993f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1331873d894a0f7eddf55636db7705a2703669e70d4555e1b131c86a130eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:18:25 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:18:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:18:35 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932fc72603790eed7a6544b8dbb7d9bb03fb889e881905748edd17ea7cc6dde`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4ee59423c4bad6b210d80822104f021daf7fe0244dba656ed9b81fa84efc7`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:4b1624ac33841e3183d8a7f27664efa4b3c021c702e7978ffde48e54de9640b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:bb3da80547699c4f867e3bdd57bd53e46b8154efc15bdcc2f927732bfa5910fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ed4499d48370ec4e0c9ceb30dcd232cab3c713f364ad43e862ebbfbada157`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:23 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:24 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098cbebc3629a723be579c26fba102101a239ec48f8ec8edd01c924e0d34f02f`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1505facc9275acd1704c663e2b285e4fd570155767fb7a37772511d037533c`  
		Last Modified: Sat, 19 Mar 2022 17:50:18 GMT  
		Size: 85.8 MB (85752952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2087f895c880bbc4a5dd55af9f50c6b41fe153944eab3ab259294d995ce03f77`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee3c8db259fbad661d1d5d5fe2dbbb14bcd8e43feda247adfd3965b7e1d3afb`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905b80ae42532bf8a83b084e9f0f088c3e1efce59abd6614102e22223337584`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:12b22ecef7f865a8702a56859b129c05c7c29073c331f4f7ca110980752bbf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17248aa017f9fce4a5570fc6a33594f9203cc3ee34d4f7d392327ac855b70544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:53 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:54 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:55 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:56 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:51:20 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:51:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:51:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:51:25 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:51:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1df472dce9231677082511ff42ef0b64a5375d4efc834bb160e6e6aae4108`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46b4d3cebbe398b4e49fe1e0d3f63ec06a91617340f20ee29f803c67f27516`  
		Last Modified: Sat, 19 Mar 2022 15:58:02 GMT  
		Size: 84.9 MB (84926141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175594e7be5b665190fd8f34399cc575fe7e3fbbe1735f9c7f80110d2a1877ea`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a9c4d9348036d86464bb1426508f43ffa8b78561e6276bef14f89a0994495`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5b16002cb5df28dcf9685d7c4fb9938503eb82bd0a3f96bb0ec192deecf4a`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a3ba3a321f6f475ec48c4b14cdd38f2d0d018313c7d2806898a0f180fd9d38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41deb8c20939b0c6294023da14f9be7c54abdf0c1007799b3e29d9199105c016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:16:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:16:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:16:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:16:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea8a0c2580c74549c69e42e4e5e4537d1bde323627baf6760ebceb984299bb2`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6ce95be154f089d489b3985d754c04b5855a86cda406b64ea9276e01aca911`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:4b1624ac33841e3183d8a7f27664efa4b3c021c702e7978ffde48e54de9640b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:bb3da80547699c4f867e3bdd57bd53e46b8154efc15bdcc2f927732bfa5910fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ed4499d48370ec4e0c9ceb30dcd232cab3c713f364ad43e862ebbfbada157`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:23 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:24 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098cbebc3629a723be579c26fba102101a239ec48f8ec8edd01c924e0d34f02f`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1505facc9275acd1704c663e2b285e4fd570155767fb7a37772511d037533c`  
		Last Modified: Sat, 19 Mar 2022 17:50:18 GMT  
		Size: 85.8 MB (85752952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2087f895c880bbc4a5dd55af9f50c6b41fe153944eab3ab259294d995ce03f77`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee3c8db259fbad661d1d5d5fe2dbbb14bcd8e43feda247adfd3965b7e1d3afb`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905b80ae42532bf8a83b084e9f0f088c3e1efce59abd6614102e22223337584`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:12b22ecef7f865a8702a56859b129c05c7c29073c331f4f7ca110980752bbf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17248aa017f9fce4a5570fc6a33594f9203cc3ee34d4f7d392327ac855b70544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:53 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:54 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:55 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:56 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:51:20 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:51:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:51:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:51:25 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:51:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1df472dce9231677082511ff42ef0b64a5375d4efc834bb160e6e6aae4108`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46b4d3cebbe398b4e49fe1e0d3f63ec06a91617340f20ee29f803c67f27516`  
		Last Modified: Sat, 19 Mar 2022 15:58:02 GMT  
		Size: 84.9 MB (84926141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175594e7be5b665190fd8f34399cc575fe7e3fbbe1735f9c7f80110d2a1877ea`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a9c4d9348036d86464bb1426508f43ffa8b78561e6276bef14f89a0994495`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5b16002cb5df28dcf9685d7c4fb9938503eb82bd0a3f96bb0ec192deecf4a`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a3ba3a321f6f475ec48c4b14cdd38f2d0d018313c7d2806898a0f180fd9d38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41deb8c20939b0c6294023da14f9be7c54abdf0c1007799b3e29d9199105c016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:16:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:16:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:16:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:16:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea8a0c2580c74549c69e42e4e5e4537d1bde323627baf6760ebceb984299bb2`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6ce95be154f089d489b3985d754c04b5855a86cda406b64ea9276e01aca911`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24`

```console
$ docker pull mariadb@sha256:4b1624ac33841e3183d8a7f27664efa4b3c021c702e7978ffde48e54de9640b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24` - linux; amd64

```console
$ docker pull mariadb@sha256:bb3da80547699c4f867e3bdd57bd53e46b8154efc15bdcc2f927732bfa5910fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ed4499d48370ec4e0c9ceb30dcd232cab3c713f364ad43e862ebbfbada157`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:23 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:24 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098cbebc3629a723be579c26fba102101a239ec48f8ec8edd01c924e0d34f02f`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1505facc9275acd1704c663e2b285e4fd570155767fb7a37772511d037533c`  
		Last Modified: Sat, 19 Mar 2022 17:50:18 GMT  
		Size: 85.8 MB (85752952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2087f895c880bbc4a5dd55af9f50c6b41fe153944eab3ab259294d995ce03f77`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee3c8db259fbad661d1d5d5fe2dbbb14bcd8e43feda247adfd3965b7e1d3afb`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905b80ae42532bf8a83b084e9f0f088c3e1efce59abd6614102e22223337584`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:12b22ecef7f865a8702a56859b129c05c7c29073c331f4f7ca110980752bbf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17248aa017f9fce4a5570fc6a33594f9203cc3ee34d4f7d392327ac855b70544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:53 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:54 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:55 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:56 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:51:20 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:51:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:51:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:51:25 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:51:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1df472dce9231677082511ff42ef0b64a5375d4efc834bb160e6e6aae4108`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46b4d3cebbe398b4e49fe1e0d3f63ec06a91617340f20ee29f803c67f27516`  
		Last Modified: Sat, 19 Mar 2022 15:58:02 GMT  
		Size: 84.9 MB (84926141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175594e7be5b665190fd8f34399cc575fe7e3fbbe1735f9c7f80110d2a1877ea`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a9c4d9348036d86464bb1426508f43ffa8b78561e6276bef14f89a0994495`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5b16002cb5df28dcf9685d7c4fb9938503eb82bd0a3f96bb0ec192deecf4a`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a3ba3a321f6f475ec48c4b14cdd38f2d0d018313c7d2806898a0f180fd9d38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41deb8c20939b0c6294023da14f9be7c54abdf0c1007799b3e29d9199105c016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:16:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:16:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:16:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:16:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea8a0c2580c74549c69e42e4e5e4537d1bde323627baf6760ebceb984299bb2`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6ce95be154f089d489b3985d754c04b5855a86cda406b64ea9276e01aca911`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24-focal`

```console
$ docker pull mariadb@sha256:4b1624ac33841e3183d8a7f27664efa4b3c021c702e7978ffde48e54de9640b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:bb3da80547699c4f867e3bdd57bd53e46b8154efc15bdcc2f927732bfa5910fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ed4499d48370ec4e0c9ceb30dcd232cab3c713f364ad43e862ebbfbada157`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 17:43:27 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:27 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 17:43:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:44:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:44:23 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:44:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:44:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 17:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:44:24 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:44:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098cbebc3629a723be579c26fba102101a239ec48f8ec8edd01c924e0d34f02f`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1505facc9275acd1704c663e2b285e4fd570155767fb7a37772511d037533c`  
		Last Modified: Sat, 19 Mar 2022 17:50:18 GMT  
		Size: 85.8 MB (85752952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2087f895c880bbc4a5dd55af9f50c6b41fe153944eab3ab259294d995ce03f77`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee3c8db259fbad661d1d5d5fe2dbbb14bcd8e43feda247adfd3965b7e1d3afb`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905b80ae42532bf8a83b084e9f0f088c3e1efce59abd6614102e22223337584`  
		Last Modified: Sat, 19 Mar 2022 17:50:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:12b22ecef7f865a8702a56859b129c05c7c29073c331f4f7ca110980752bbf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17248aa017f9fce4a5570fc6a33594f9203cc3ee34d4f7d392327ac855b70544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:53 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:54 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 15:50:55 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:56 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 15:50:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:51:20 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:51:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:51:23 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 15:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:51:25 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:51:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1df472dce9231677082511ff42ef0b64a5375d4efc834bb160e6e6aae4108`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46b4d3cebbe398b4e49fe1e0d3f63ec06a91617340f20ee29f803c67f27516`  
		Last Modified: Sat, 19 Mar 2022 15:58:02 GMT  
		Size: 84.9 MB (84926141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175594e7be5b665190fd8f34399cc575fe7e3fbbe1735f9c7f80110d2a1877ea`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a9c4d9348036d86464bb1426508f43ffa8b78561e6276bef14f89a0994495`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5b16002cb5df28dcf9685d7c4fb9938503eb82bd0a3f96bb0ec192deecf4a`  
		Last Modified: Sat, 19 Mar 2022 15:57:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a3ba3a321f6f475ec48c4b14cdd38f2d0d018313c7d2806898a0f180fd9d38d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41deb8c20939b0c6294023da14f9be7c54abdf0c1007799b3e29d9199105c016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:16:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 19 Mar 2022 21:16:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:16:15 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:16:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea8a0c2580c74549c69e42e4e5e4537d1bde323627baf6760ebceb984299bb2`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6ce95be154f089d489b3985d754c04b5855a86cda406b64ea9276e01aca911`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:608b9e3c129f62efa7ebb93a5373c04784b91a89275d794ac2f2099fe1d6daa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:e165633268d7fb8e668c9eb0192ab513239b6fc532b7e83b3fc3f94ede4e8208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127924242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6149372f976138f2fda256a4d4ea24946c6b0b588e2e0183d405f484b94262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:43:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:43:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:43:22 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:43:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d35769a106e22aae0cf016dbbf1a382ff0547950fe831ab09d59e7f1dadffa`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdced1d466cffb81011140b11ed7fa9bc42724aae42b9185d8de9da8ef476c0`  
		Last Modified: Sat, 19 Mar 2022 17:49:48 GMT  
		Size: 88.0 MB (87996850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff170e7bd504167e4637934435c0f43df732bea20a34429a90a6e4656ddb5ad`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35ba3c06407618e8e80d66814d1d0d7954957fcbacf7ddad38817acd78a21f`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:627bd88adcc659733fc3e576728915e89261c0fddffb9cb96fdc05397375acd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125188494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef32e28ab3918d4b35878e96bb8361787841f3482213e91edcff8b13ae9b02fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:16 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:17 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:18 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:19 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:46 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425cd182719491d12cfa6d36e8374717a86de57e73a3c3fdd8a3af11f013e994`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e673b6cea313c1da83d658ff73139b7a028c7cddec48705c3aa9faa3a208bdde`  
		Last Modified: Sat, 19 Mar 2022 15:57:31 GMT  
		Size: 87.1 MB (87109165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d965d1dba66e258c1873b60d95b930eeb7ed9880e03e8af2fed6e6d26acbd`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524dafeadc06e50b362f40d9cf685922259052e83c18ebd0840ccbba8fb22b0`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:88ecf463c071c97c6023c2301d546d8e3d4f47b93352944377c57d4f57ece54a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fa809924a6ad3bf6725ca560daeaa7e263f6a6a9f43862033c698863e5270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:13:51 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:13:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:13:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5e55a9d1a681d0184d41c0d42de24aeeeb38e8968e389bc4be842beeaa428`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:d377d95888a54801139e1e6d6720c24ea3552a978a2bdc1cabfc6e9bbfd91c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ada2fc773199ea616a476974307e6436555c80eade61ed32791c3633e3f68b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:36:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:36:01 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:36:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d88422d0d73343c9be0ae62933dd57cd450bcf96b9608e2d3719e1401c58e6`  
		Last Modified: Fri, 18 Mar 2022 17:38:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdcf97c1cd0b3200c067f0d6bde2564cb6deb4ee04bbfba8f7a144b42d8176`  
		Last Modified: Fri, 18 Mar 2022 17:38:24 GMT  
		Size: 89.3 MB (89290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380909a019962d86a49869c750e137beff19db7d9c3342360725ae700a42618b`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af30cc7b6870ef44d618c5fc69b52ffdac66b0d927048462554401008e88af56`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:608b9e3c129f62efa7ebb93a5373c04784b91a89275d794ac2f2099fe1d6daa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:e165633268d7fb8e668c9eb0192ab513239b6fc532b7e83b3fc3f94ede4e8208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127924242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6149372f976138f2fda256a4d4ea24946c6b0b588e2e0183d405f484b94262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:43:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:43:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:43:22 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:43:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d35769a106e22aae0cf016dbbf1a382ff0547950fe831ab09d59e7f1dadffa`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdced1d466cffb81011140b11ed7fa9bc42724aae42b9185d8de9da8ef476c0`  
		Last Modified: Sat, 19 Mar 2022 17:49:48 GMT  
		Size: 88.0 MB (87996850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff170e7bd504167e4637934435c0f43df732bea20a34429a90a6e4656ddb5ad`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35ba3c06407618e8e80d66814d1d0d7954957fcbacf7ddad38817acd78a21f`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:627bd88adcc659733fc3e576728915e89261c0fddffb9cb96fdc05397375acd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125188494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef32e28ab3918d4b35878e96bb8361787841f3482213e91edcff8b13ae9b02fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:16 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:17 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:18 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:19 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:46 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425cd182719491d12cfa6d36e8374717a86de57e73a3c3fdd8a3af11f013e994`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e673b6cea313c1da83d658ff73139b7a028c7cddec48705c3aa9faa3a208bdde`  
		Last Modified: Sat, 19 Mar 2022 15:57:31 GMT  
		Size: 87.1 MB (87109165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d965d1dba66e258c1873b60d95b930eeb7ed9880e03e8af2fed6e6d26acbd`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524dafeadc06e50b362f40d9cf685922259052e83c18ebd0840ccbba8fb22b0`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:88ecf463c071c97c6023c2301d546d8e3d4f47b93352944377c57d4f57ece54a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fa809924a6ad3bf6725ca560daeaa7e263f6a6a9f43862033c698863e5270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:13:51 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:13:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:13:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5e55a9d1a681d0184d41c0d42de24aeeeb38e8968e389bc4be842beeaa428`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d377d95888a54801139e1e6d6720c24ea3552a978a2bdc1cabfc6e9bbfd91c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ada2fc773199ea616a476974307e6436555c80eade61ed32791c3633e3f68b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:36:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:36:01 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:36:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d88422d0d73343c9be0ae62933dd57cd450bcf96b9608e2d3719e1401c58e6`  
		Last Modified: Fri, 18 Mar 2022 17:38:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdcf97c1cd0b3200c067f0d6bde2564cb6deb4ee04bbfba8f7a144b42d8176`  
		Last Modified: Fri, 18 Mar 2022 17:38:24 GMT  
		Size: 89.3 MB (89290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380909a019962d86a49869c750e137beff19db7d9c3342360725ae700a42618b`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af30cc7b6870ef44d618c5fc69b52ffdac66b0d927048462554401008e88af56`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15`

```console
$ docker pull mariadb@sha256:608b9e3c129f62efa7ebb93a5373c04784b91a89275d794ac2f2099fe1d6daa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15` - linux; amd64

```console
$ docker pull mariadb@sha256:e165633268d7fb8e668c9eb0192ab513239b6fc532b7e83b3fc3f94ede4e8208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127924242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6149372f976138f2fda256a4d4ea24946c6b0b588e2e0183d405f484b94262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:43:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:43:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:43:22 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:43:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d35769a106e22aae0cf016dbbf1a382ff0547950fe831ab09d59e7f1dadffa`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdced1d466cffb81011140b11ed7fa9bc42724aae42b9185d8de9da8ef476c0`  
		Last Modified: Sat, 19 Mar 2022 17:49:48 GMT  
		Size: 88.0 MB (87996850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff170e7bd504167e4637934435c0f43df732bea20a34429a90a6e4656ddb5ad`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35ba3c06407618e8e80d66814d1d0d7954957fcbacf7ddad38817acd78a21f`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:627bd88adcc659733fc3e576728915e89261c0fddffb9cb96fdc05397375acd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125188494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef32e28ab3918d4b35878e96bb8361787841f3482213e91edcff8b13ae9b02fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:16 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:17 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:18 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:19 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:46 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425cd182719491d12cfa6d36e8374717a86de57e73a3c3fdd8a3af11f013e994`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e673b6cea313c1da83d658ff73139b7a028c7cddec48705c3aa9faa3a208bdde`  
		Last Modified: Sat, 19 Mar 2022 15:57:31 GMT  
		Size: 87.1 MB (87109165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d965d1dba66e258c1873b60d95b930eeb7ed9880e03e8af2fed6e6d26acbd`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524dafeadc06e50b362f40d9cf685922259052e83c18ebd0840ccbba8fb22b0`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; ppc64le

```console
$ docker pull mariadb@sha256:88ecf463c071c97c6023c2301d546d8e3d4f47b93352944377c57d4f57ece54a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fa809924a6ad3bf6725ca560daeaa7e263f6a6a9f43862033c698863e5270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:13:51 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:13:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:13:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5e55a9d1a681d0184d41c0d42de24aeeeb38e8968e389bc4be842beeaa428`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; s390x

```console
$ docker pull mariadb@sha256:d377d95888a54801139e1e6d6720c24ea3552a978a2bdc1cabfc6e9bbfd91c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ada2fc773199ea616a476974307e6436555c80eade61ed32791c3633e3f68b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:36:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:36:01 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:36:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d88422d0d73343c9be0ae62933dd57cd450bcf96b9608e2d3719e1401c58e6`  
		Last Modified: Fri, 18 Mar 2022 17:38:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdcf97c1cd0b3200c067f0d6bde2564cb6deb4ee04bbfba8f7a144b42d8176`  
		Last Modified: Fri, 18 Mar 2022 17:38:24 GMT  
		Size: 89.3 MB (89290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380909a019962d86a49869c750e137beff19db7d9c3342360725ae700a42618b`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af30cc7b6870ef44d618c5fc69b52ffdac66b0d927048462554401008e88af56`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15-focal`

```console
$ docker pull mariadb@sha256:608b9e3c129f62efa7ebb93a5373c04784b91a89275d794ac2f2099fe1d6daa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:e165633268d7fb8e668c9eb0192ab513239b6fc532b7e83b3fc3f94ede4e8208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127924242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6149372f976138f2fda256a4d4ea24946c6b0b588e2e0183d405f484b94262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 17:42:59 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 17:42:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:43:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:43:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:43:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:43:22 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:43:22 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:43:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d35769a106e22aae0cf016dbbf1a382ff0547950fe831ab09d59e7f1dadffa`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdced1d466cffb81011140b11ed7fa9bc42724aae42b9185d8de9da8ef476c0`  
		Last Modified: Sat, 19 Mar 2022 17:49:48 GMT  
		Size: 88.0 MB (87996850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff170e7bd504167e4637934435c0f43df732bea20a34429a90a6e4656ddb5ad`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35ba3c06407618e8e80d66814d1d0d7954957fcbacf7ddad38817acd78a21f`  
		Last Modified: Sat, 19 Mar 2022 17:49:34 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:627bd88adcc659733fc3e576728915e89261c0fddffb9cb96fdc05397375acd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125188494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef32e28ab3918d4b35878e96bb8361787841f3482213e91edcff8b13ae9b02fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:50:16 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:17 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 15:50:18 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:19 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 15:50:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:50:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:42 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:45 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:46 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425cd182719491d12cfa6d36e8374717a86de57e73a3c3fdd8a3af11f013e994`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e673b6cea313c1da83d658ff73139b7a028c7cddec48705c3aa9faa3a208bdde`  
		Last Modified: Sat, 19 Mar 2022 15:57:31 GMT  
		Size: 87.1 MB (87109165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d965d1dba66e258c1873b60d95b930eeb7ed9880e03e8af2fed6e6d26acbd`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524dafeadc06e50b362f40d9cf685922259052e83c18ebd0840ccbba8fb22b0`  
		Last Modified: Sat, 19 Mar 2022 15:57:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:88ecf463c071c97c6023c2301d546d8e3d4f47b93352944377c57d4f57ece54a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1fa809924a6ad3bf6725ca560daeaa7e263f6a6a9f43862033c698863e5270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:13:51 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:13:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:13:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5e55a9d1a681d0184d41c0d42de24aeeeb38e8968e389bc4be842beeaa428`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d377d95888a54801139e1e6d6720c24ea3552a978a2bdc1cabfc6e9bbfd91c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ada2fc773199ea616a476974307e6436555c80eade61ed32791c3633e3f68b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Mar 2022 17:35:34 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 18 Mar 2022 17:35:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:36:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:36:01 GMT
COPY file:3bfbd31c0a9278a94216849008ad3bcbc06de4ed6ad1cfc9a1c6a511007ea3c4 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:36:01 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:36:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d88422d0d73343c9be0ae62933dd57cd450bcf96b9608e2d3719e1401c58e6`  
		Last Modified: Fri, 18 Mar 2022 17:38:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdcf97c1cd0b3200c067f0d6bde2564cb6deb4ee04bbfba8f7a144b42d8176`  
		Last Modified: Fri, 18 Mar 2022 17:38:24 GMT  
		Size: 89.3 MB (89290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380909a019962d86a49869c750e137beff19db7d9c3342360725ae700a42618b`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af30cc7b6870ef44d618c5fc69b52ffdac66b0d927048462554401008e88af56`  
		Last Modified: Fri, 18 Mar 2022 17:38:10 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:98f64723548cacaf3a608961c8c7aca45cc79c1eb5be6abfc4c2ebe581110c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:32fe40d4f1168ac4fab661ab4c1f7178ebbabd113b8010531943063e2e7c3608
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128170568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05effe5d089696d5a99fd5d69e9a30c389544689c6d729eb1e722de793c568b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:56 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edfddc2625d754f3e9f0d5bf7f09bd30c839b1d369783bbb11c619de571491e`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed63bea44051024324cca8155dbd7a844a0acba758a4c41b2b05c49efcde99`  
		Last Modified: Sat, 19 Mar 2022 17:49:18 GMT  
		Size: 88.2 MB (88243171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edcfa88ae71bd52788feaedcc3dffc8b38079a24f074a32e7125f802e9c9f3`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2decc8c9a34661ee85a5dbc038b97146dc561d3f5fe570bb17c2b027ebb25f`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:02ee99be1542e23d6a7907a1f3b952f720c3ef7785f9a16f9934e66c5cefe265
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec12ecb0d0b4638666e674e55aa2bd06355063fdc66531c037f033d9fd2ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:39 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:40 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:41 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:42 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:07 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:08 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:09 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137676fb42f9c4e85719b9cd7999eaf4258e73204d5c53b2978eeb234c7ba27`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a727aaa4bcdee1c65ed79fd8e4ad118eb6f43ecee9d44bc8c13e29cd17bcaf1`  
		Last Modified: Sat, 19 Mar 2022 15:56:59 GMT  
		Size: 87.2 MB (87193081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5fc0731a563fc3bb10b3ce1e856d5e52d0318ac888e271899ec2903036c036`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33530e1edbed0d8fd58d803293ba5107165f7bad7d69424c3197a353eadb06b3`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f4d02d059596433fa6dd6849259884649b95b343e0d955ff11b529175e13d807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3106fca0021d0eb0a01f1c141c7a466efcd86ecfa7ffbd22c57a9b00d40ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:11:49 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:11:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:11:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78d531db0236b9ad0f80b51c12c7d4194eef5c4c178df0c69384bb30512c194`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:45d2ed3746f034ba567df464418d77176ac10668824f85894eb19d29e065e1c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d1581143c8ad590cd4d750aa38f504dc98a4e4f88e18a6b3a298cac52c61a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:35:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:35:26 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:35:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59262dbc7499e1332bb0d0ff3cd4bd5ece29ed8badc8c505ce076c3c15bb1e`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea8278be92764790f029c13fde2cd901d23dd21c3a0ff1fee7d43b65e718af`  
		Last Modified: Fri, 18 Mar 2022 17:38:00 GMT  
		Size: 89.3 MB (89316761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07ea2b862c1cf9f56a42f2a60b3c63eee47ff9d5710d0a80025e8f6e177eba`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806dd7cfb15dd6477605887020c0ade0a17e804e9136da6089f1da155cc312c`  
		Last Modified: Fri, 18 Mar 2022 17:37:48 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:98f64723548cacaf3a608961c8c7aca45cc79c1eb5be6abfc4c2ebe581110c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:32fe40d4f1168ac4fab661ab4c1f7178ebbabd113b8010531943063e2e7c3608
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128170568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05effe5d089696d5a99fd5d69e9a30c389544689c6d729eb1e722de793c568b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:56 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edfddc2625d754f3e9f0d5bf7f09bd30c839b1d369783bbb11c619de571491e`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed63bea44051024324cca8155dbd7a844a0acba758a4c41b2b05c49efcde99`  
		Last Modified: Sat, 19 Mar 2022 17:49:18 GMT  
		Size: 88.2 MB (88243171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edcfa88ae71bd52788feaedcc3dffc8b38079a24f074a32e7125f802e9c9f3`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2decc8c9a34661ee85a5dbc038b97146dc561d3f5fe570bb17c2b027ebb25f`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:02ee99be1542e23d6a7907a1f3b952f720c3ef7785f9a16f9934e66c5cefe265
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec12ecb0d0b4638666e674e55aa2bd06355063fdc66531c037f033d9fd2ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:39 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:40 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:41 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:42 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:07 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:08 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:09 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137676fb42f9c4e85719b9cd7999eaf4258e73204d5c53b2978eeb234c7ba27`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a727aaa4bcdee1c65ed79fd8e4ad118eb6f43ecee9d44bc8c13e29cd17bcaf1`  
		Last Modified: Sat, 19 Mar 2022 15:56:59 GMT  
		Size: 87.2 MB (87193081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5fc0731a563fc3bb10b3ce1e856d5e52d0318ac888e271899ec2903036c036`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33530e1edbed0d8fd58d803293ba5107165f7bad7d69424c3197a353eadb06b3`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f4d02d059596433fa6dd6849259884649b95b343e0d955ff11b529175e13d807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3106fca0021d0eb0a01f1c141c7a466efcd86ecfa7ffbd22c57a9b00d40ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:11:49 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:11:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:11:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78d531db0236b9ad0f80b51c12c7d4194eef5c4c178df0c69384bb30512c194`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:45d2ed3746f034ba567df464418d77176ac10668824f85894eb19d29e065e1c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d1581143c8ad590cd4d750aa38f504dc98a4e4f88e18a6b3a298cac52c61a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:35:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:35:26 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:35:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59262dbc7499e1332bb0d0ff3cd4bd5ece29ed8badc8c505ce076c3c15bb1e`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea8278be92764790f029c13fde2cd901d23dd21c3a0ff1fee7d43b65e718af`  
		Last Modified: Fri, 18 Mar 2022 17:38:00 GMT  
		Size: 89.3 MB (89316761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07ea2b862c1cf9f56a42f2a60b3c63eee47ff9d5710d0a80025e8f6e177eba`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806dd7cfb15dd6477605887020c0ade0a17e804e9136da6089f1da155cc312c`  
		Last Modified: Fri, 18 Mar 2022 17:37:48 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7`

```console
$ docker pull mariadb@sha256:98f64723548cacaf3a608961c8c7aca45cc79c1eb5be6abfc4c2ebe581110c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7` - linux; amd64

```console
$ docker pull mariadb@sha256:32fe40d4f1168ac4fab661ab4c1f7178ebbabd113b8010531943063e2e7c3608
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128170568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05effe5d089696d5a99fd5d69e9a30c389544689c6d729eb1e722de793c568b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:56 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edfddc2625d754f3e9f0d5bf7f09bd30c839b1d369783bbb11c619de571491e`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed63bea44051024324cca8155dbd7a844a0acba758a4c41b2b05c49efcde99`  
		Last Modified: Sat, 19 Mar 2022 17:49:18 GMT  
		Size: 88.2 MB (88243171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edcfa88ae71bd52788feaedcc3dffc8b38079a24f074a32e7125f802e9c9f3`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2decc8c9a34661ee85a5dbc038b97146dc561d3f5fe570bb17c2b027ebb25f`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:02ee99be1542e23d6a7907a1f3b952f720c3ef7785f9a16f9934e66c5cefe265
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec12ecb0d0b4638666e674e55aa2bd06355063fdc66531c037f033d9fd2ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:39 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:40 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:41 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:42 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:07 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:08 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:09 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137676fb42f9c4e85719b9cd7999eaf4258e73204d5c53b2978eeb234c7ba27`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a727aaa4bcdee1c65ed79fd8e4ad118eb6f43ecee9d44bc8c13e29cd17bcaf1`  
		Last Modified: Sat, 19 Mar 2022 15:56:59 GMT  
		Size: 87.2 MB (87193081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5fc0731a563fc3bb10b3ce1e856d5e52d0318ac888e271899ec2903036c036`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33530e1edbed0d8fd58d803293ba5107165f7bad7d69424c3197a353eadb06b3`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f4d02d059596433fa6dd6849259884649b95b343e0d955ff11b529175e13d807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3106fca0021d0eb0a01f1c141c7a466efcd86ecfa7ffbd22c57a9b00d40ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:11:49 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:11:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:11:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78d531db0236b9ad0f80b51c12c7d4194eef5c4c178df0c69384bb30512c194`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; s390x

```console
$ docker pull mariadb@sha256:45d2ed3746f034ba567df464418d77176ac10668824f85894eb19d29e065e1c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d1581143c8ad590cd4d750aa38f504dc98a4e4f88e18a6b3a298cac52c61a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:35:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:35:26 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:35:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59262dbc7499e1332bb0d0ff3cd4bd5ece29ed8badc8c505ce076c3c15bb1e`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea8278be92764790f029c13fde2cd901d23dd21c3a0ff1fee7d43b65e718af`  
		Last Modified: Fri, 18 Mar 2022 17:38:00 GMT  
		Size: 89.3 MB (89316761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07ea2b862c1cf9f56a42f2a60b3c63eee47ff9d5710d0a80025e8f6e177eba`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806dd7cfb15dd6477605887020c0ade0a17e804e9136da6089f1da155cc312c`  
		Last Modified: Fri, 18 Mar 2022 17:37:48 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7-focal`

```console
$ docker pull mariadb@sha256:98f64723548cacaf3a608961c8c7aca45cc79c1eb5be6abfc4c2ebe581110c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:32fe40d4f1168ac4fab661ab4c1f7178ebbabd113b8010531943063e2e7c3608
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128170568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05effe5d089696d5a99fd5d69e9a30c389544689c6d729eb1e722de793c568b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 17:42:31 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 17:42:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:56 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:56 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:56 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edfddc2625d754f3e9f0d5bf7f09bd30c839b1d369783bbb11c619de571491e`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed63bea44051024324cca8155dbd7a844a0acba758a4c41b2b05c49efcde99`  
		Last Modified: Sat, 19 Mar 2022 17:49:18 GMT  
		Size: 88.2 MB (88243171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edcfa88ae71bd52788feaedcc3dffc8b38079a24f074a32e7125f802e9c9f3`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2decc8c9a34661ee85a5dbc038b97146dc561d3f5fe570bb17c2b027ebb25f`  
		Last Modified: Sat, 19 Mar 2022 17:49:03 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:02ee99be1542e23d6a7907a1f3b952f720c3ef7785f9a16f9934e66c5cefe265
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec12ecb0d0b4638666e674e55aa2bd06355063fdc66531c037f033d9fd2ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:39 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:40 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 15:49:41 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:42 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 15:49:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:50:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:50:07 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:50:08 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:50:09 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:50:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137676fb42f9c4e85719b9cd7999eaf4258e73204d5c53b2978eeb234c7ba27`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a727aaa4bcdee1c65ed79fd8e4ad118eb6f43ecee9d44bc8c13e29cd17bcaf1`  
		Last Modified: Sat, 19 Mar 2022 15:56:59 GMT  
		Size: 87.2 MB (87193081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5fc0731a563fc3bb10b3ce1e856d5e52d0318ac888e271899ec2903036c036`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33530e1edbed0d8fd58d803293ba5107165f7bad7d69424c3197a353eadb06b3`  
		Last Modified: Sat, 19 Mar 2022 15:56:45 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f4d02d059596433fa6dd6849259884649b95b343e0d955ff11b529175e13d807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3106fca0021d0eb0a01f1c141c7a466efcd86ecfa7ffbd22c57a9b00d40ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:11:49 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:11:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:11:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78d531db0236b9ad0f80b51c12c7d4194eef5c4c178df0c69384bb30512c194`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:45d2ed3746f034ba567df464418d77176ac10668824f85894eb19d29e065e1c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d1581143c8ad590cd4d750aa38f504dc98a4e4f88e18a6b3a298cac52c61a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Mar 2022 17:34:57 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 18 Mar 2022 17:34:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:35:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:35:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:35:26 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:35:26 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:35:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59262dbc7499e1332bb0d0ff3cd4bd5ece29ed8badc8c505ce076c3c15bb1e`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea8278be92764790f029c13fde2cd901d23dd21c3a0ff1fee7d43b65e718af`  
		Last Modified: Fri, 18 Mar 2022 17:38:00 GMT  
		Size: 89.3 MB (89316761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07ea2b862c1cf9f56a42f2a60b3c63eee47ff9d5710d0a80025e8f6e177eba`  
		Last Modified: Fri, 18 Mar 2022 17:37:47 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806dd7cfb15dd6477605887020c0ade0a17e804e9136da6089f1da155cc312c`  
		Last Modified: Fri, 18 Mar 2022 17:37:48 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3-focal`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc`

```console
$ docker pull mariadb@sha256:70b339fadd483679c027cc2cded0cf201d9b8e1a54f0dbc231268ae4ba5d4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:c13dc04f62db473e08d0d236aeb1858c1e2e38bc57c94035d405b7caebd16560
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128579219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206021348858f8ee4e6d8675d3e8e1b0db1fd1108451ec47d8687fcda2434d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:41:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:41:53 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:41:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:41:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb8f2920e8fae0c7e5398efc97b8322b4c023dfe141725d4bda58ff3a5fc651`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd2347cbcb79551d6a212844394d3ebc1b207110fe9a150103f362de5c4861`  
		Last Modified: Sat, 19 Mar 2022 17:48:04 GMT  
		Size: 88.7 MB (88651820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2948520939c277f617aa737ab4590c910d84491b07f2e17ebcb6f4829a419`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1603bc329d2cdd670cc7ed6830f444558f1f1a87ece843f92ddb8e75684f4e`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b24e5947e5403890e134cc908e8a2d615b203c5b491e7bb44203a2770aa5de95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37abf771ba25a66a49cec1ed690d0d28f07737b10931006e1c4ef37645bfcc4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:48:21 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:22 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:23 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:24 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:48:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:48:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:48:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:48:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:48:51 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:48:52 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:48:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7c805732bec26fd5a137c043b0d193d6149eaaa043fcb6bdc89bd730dfc838`  
		Last Modified: Sat, 19 Mar 2022 15:55:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baba00d3871be9fe26b97b71570c4bbbf2740d68121cf10894b445a1a9c1ed`  
		Last Modified: Sat, 19 Mar 2022 15:55:39 GMT  
		Size: 87.6 MB (87574071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd271a2b44012ae5ed49420434d551643a94dc499ce9551663bb8f8e3e627a30`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65948626571f6898a98b02c1c1b73f2cb4831a9c1924ac327256a72bd53d9fee`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f3616155c90dfef40d2968bdc2012f40bc9906c6d2e978f60a032303bd13b91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afc8666accf61f72ef2c41a00fab1d1f8359cf168c98f5066b8414140250828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:06:42 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:06:44 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:06:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3237f0125a75831c83f9d5f71a63fa0a840a0c55801d276e5ff89b091cabc95`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:2e3acb368b2f1a89658f47d2bd73a5f7ebcdafd88e1654877a3154fae116ab6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127688366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c79cfb644e35b1e29ada2deca102cb718a63e66371b043b66a0c029852cc0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:33:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:13 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f50e84e90bd214e9540e47185aac0ba39ca448e6fd67a8ad9f41f8bcaaea8c0`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e46264989865f2f7721b47848a1a4170b6ce78d94422c10ceb1e36e338f4d`  
		Last Modified: Fri, 18 Mar 2022 17:37:06 GMT  
		Size: 89.8 MB (89780305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373bc9333b1bf4f6d9c44543a5596ac30e340c185d6e6cc9f0a05044e53f344c`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1987b8950b424889557febb98f00d969f2691edc19019d999630666b17d9ad4`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc-focal`

```console
$ docker pull mariadb@sha256:70b339fadd483679c027cc2cded0cf201d9b8e1a54f0dbc231268ae4ba5d4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c13dc04f62db473e08d0d236aeb1858c1e2e38bc57c94035d405b7caebd16560
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128579219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206021348858f8ee4e6d8675d3e8e1b0db1fd1108451ec47d8687fcda2434d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:41:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:41:53 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:41:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:41:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb8f2920e8fae0c7e5398efc97b8322b4c023dfe141725d4bda58ff3a5fc651`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd2347cbcb79551d6a212844394d3ebc1b207110fe9a150103f362de5c4861`  
		Last Modified: Sat, 19 Mar 2022 17:48:04 GMT  
		Size: 88.7 MB (88651820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2948520939c277f617aa737ab4590c910d84491b07f2e17ebcb6f4829a419`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1603bc329d2cdd670cc7ed6830f444558f1f1a87ece843f92ddb8e75684f4e`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b24e5947e5403890e134cc908e8a2d615b203c5b491e7bb44203a2770aa5de95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37abf771ba25a66a49cec1ed690d0d28f07737b10931006e1c4ef37645bfcc4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:48:21 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:22 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:23 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:24 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:48:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:48:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:48:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:48:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:48:51 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:48:52 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:48:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7c805732bec26fd5a137c043b0d193d6149eaaa043fcb6bdc89bd730dfc838`  
		Last Modified: Sat, 19 Mar 2022 15:55:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baba00d3871be9fe26b97b71570c4bbbf2740d68121cf10894b445a1a9c1ed`  
		Last Modified: Sat, 19 Mar 2022 15:55:39 GMT  
		Size: 87.6 MB (87574071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd271a2b44012ae5ed49420434d551643a94dc499ce9551663bb8f8e3e627a30`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65948626571f6898a98b02c1c1b73f2cb4831a9c1924ac327256a72bd53d9fee`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f3616155c90dfef40d2968bdc2012f40bc9906c6d2e978f60a032303bd13b91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afc8666accf61f72ef2c41a00fab1d1f8359cf168c98f5066b8414140250828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:06:42 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:06:44 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:06:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3237f0125a75831c83f9d5f71a63fa0a840a0c55801d276e5ff89b091cabc95`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2e3acb368b2f1a89658f47d2bd73a5f7ebcdafd88e1654877a3154fae116ab6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127688366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c79cfb644e35b1e29ada2deca102cb718a63e66371b043b66a0c029852cc0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:33:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:13 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f50e84e90bd214e9540e47185aac0ba39ca448e6fd67a8ad9f41f8bcaaea8c0`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e46264989865f2f7721b47848a1a4170b6ce78d94422c10ceb1e36e338f4d`  
		Last Modified: Fri, 18 Mar 2022 17:37:06 GMT  
		Size: 89.8 MB (89780305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373bc9333b1bf4f6d9c44543a5596ac30e340c185d6e6cc9f0a05044e53f344c`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1987b8950b424889557febb98f00d969f2691edc19019d999630666b17d9ad4`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc`

```console
$ docker pull mariadb@sha256:70b339fadd483679c027cc2cded0cf201d9b8e1a54f0dbc231268ae4ba5d4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:c13dc04f62db473e08d0d236aeb1858c1e2e38bc57c94035d405b7caebd16560
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128579219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206021348858f8ee4e6d8675d3e8e1b0db1fd1108451ec47d8687fcda2434d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:41:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:41:53 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:41:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:41:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb8f2920e8fae0c7e5398efc97b8322b4c023dfe141725d4bda58ff3a5fc651`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd2347cbcb79551d6a212844394d3ebc1b207110fe9a150103f362de5c4861`  
		Last Modified: Sat, 19 Mar 2022 17:48:04 GMT  
		Size: 88.7 MB (88651820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2948520939c277f617aa737ab4590c910d84491b07f2e17ebcb6f4829a419`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1603bc329d2cdd670cc7ed6830f444558f1f1a87ece843f92ddb8e75684f4e`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b24e5947e5403890e134cc908e8a2d615b203c5b491e7bb44203a2770aa5de95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37abf771ba25a66a49cec1ed690d0d28f07737b10931006e1c4ef37645bfcc4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:48:21 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:22 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:23 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:24 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:48:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:48:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:48:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:48:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:48:51 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:48:52 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:48:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7c805732bec26fd5a137c043b0d193d6149eaaa043fcb6bdc89bd730dfc838`  
		Last Modified: Sat, 19 Mar 2022 15:55:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baba00d3871be9fe26b97b71570c4bbbf2740d68121cf10894b445a1a9c1ed`  
		Last Modified: Sat, 19 Mar 2022 15:55:39 GMT  
		Size: 87.6 MB (87574071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd271a2b44012ae5ed49420434d551643a94dc499ce9551663bb8f8e3e627a30`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65948626571f6898a98b02c1c1b73f2cb4831a9c1924ac327256a72bd53d9fee`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f3616155c90dfef40d2968bdc2012f40bc9906c6d2e978f60a032303bd13b91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afc8666accf61f72ef2c41a00fab1d1f8359cf168c98f5066b8414140250828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:06:42 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:06:44 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:06:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3237f0125a75831c83f9d5f71a63fa0a840a0c55801d276e5ff89b091cabc95`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:2e3acb368b2f1a89658f47d2bd73a5f7ebcdafd88e1654877a3154fae116ab6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127688366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c79cfb644e35b1e29ada2deca102cb718a63e66371b043b66a0c029852cc0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:33:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:13 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f50e84e90bd214e9540e47185aac0ba39ca448e6fd67a8ad9f41f8bcaaea8c0`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e46264989865f2f7721b47848a1a4170b6ce78d94422c10ceb1e36e338f4d`  
		Last Modified: Fri, 18 Mar 2022 17:37:06 GMT  
		Size: 89.8 MB (89780305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373bc9333b1bf4f6d9c44543a5596ac30e340c185d6e6cc9f0a05044e53f344c`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1987b8950b424889557febb98f00d969f2691edc19019d999630666b17d9ad4`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc-focal`

```console
$ docker pull mariadb@sha256:70b339fadd483679c027cc2cded0cf201d9b8e1a54f0dbc231268ae4ba5d4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c13dc04f62db473e08d0d236aeb1858c1e2e38bc57c94035d405b7caebd16560
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128579219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206021348858f8ee4e6d8675d3e8e1b0db1fd1108451ec47d8687fcda2434d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 17:41:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 17:41:16 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:41:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:41:53 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:41:53 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:41:53 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:41:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb8f2920e8fae0c7e5398efc97b8322b4c023dfe141725d4bda58ff3a5fc651`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd2347cbcb79551d6a212844394d3ebc1b207110fe9a150103f362de5c4861`  
		Last Modified: Sat, 19 Mar 2022 17:48:04 GMT  
		Size: 88.7 MB (88651820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2948520939c277f617aa737ab4590c910d84491b07f2e17ebcb6f4829a419`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1603bc329d2cdd670cc7ed6830f444558f1f1a87ece843f92ddb8e75684f4e`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b24e5947e5403890e134cc908e8a2d615b203c5b491e7bb44203a2770aa5de95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37abf771ba25a66a49cec1ed690d0d28f07737b10931006e1c4ef37645bfcc4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:48:21 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:22 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 15:48:23 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:24 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 15:48:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:48:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:48:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:48:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:48:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:48:51 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:48:52 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:48:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7c805732bec26fd5a137c043b0d193d6149eaaa043fcb6bdc89bd730dfc838`  
		Last Modified: Sat, 19 Mar 2022 15:55:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baba00d3871be9fe26b97b71570c4bbbf2740d68121cf10894b445a1a9c1ed`  
		Last Modified: Sat, 19 Mar 2022 15:55:39 GMT  
		Size: 87.6 MB (87574071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd271a2b44012ae5ed49420434d551643a94dc499ce9551663bb8f8e3e627a30`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65948626571f6898a98b02c1c1b73f2cb4831a9c1924ac327256a72bd53d9fee`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3f3616155c90dfef40d2968bdc2012f40bc9906c6d2e978f60a032303bd13b91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afc8666accf61f72ef2c41a00fab1d1f8359cf168c98f5066b8414140250828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:06:42 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:06:44 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:06:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3237f0125a75831c83f9d5f71a63fa0a840a0c55801d276e5ff89b091cabc95`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2e3acb368b2f1a89658f47d2bd73a5f7ebcdafd88e1654877a3154fae116ab6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127688366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c79cfb644e35b1e29ada2deca102cb718a63e66371b043b66a0c029852cc0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 18 Mar 2022 17:33:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 18 Mar 2022 17:33:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:33:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:13 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:13 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f50e84e90bd214e9540e47185aac0ba39ca448e6fd67a8ad9f41f8bcaaea8c0`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e46264989865f2f7721b47848a1a4170b6ce78d94422c10ceb1e36e338f4d`  
		Last Modified: Fri, 18 Mar 2022 17:37:06 GMT  
		Size: 89.8 MB (89780305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373bc9333b1bf4f6d9c44543a5596ac30e340c185d6e6cc9f0a05044e53f344c`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1987b8950b424889557febb98f00d969f2691edc19019d999630666b17d9ad4`  
		Last Modified: Fri, 18 Mar 2022 17:36:52 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:f2eddab27776f16767ea3473143abbebcf40e7d122874dc90763439b90b7d7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:73439feeb72623d837f6aa7110e8bfcd8629aec6a4c56ad139de886b5973468f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128669169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0162b44a5fa3792ebcfefa147cf85829c2a41284bbb1b3e5b1965667ace830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 17:39:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 17:40:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:12 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 17:40:25 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 17:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 17:40:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 17:40:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 17:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 17:42:03 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 17:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 17:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 17:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 17:42:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 17:42:27 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 17:42:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03231033a6687aa95f844c682c8619e10937a1970b778429eb347e0b6d1f4bd8`  
		Last Modified: Sat, 19 Mar 2022 17:47:54 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8bcd9a929e46f016cb4f44a857eb33633337c6624331d24615fe39bfc0994`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 5.5 MB (5488521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c260950e90fb7e63889c9f4671524cfff23f4392d7a63fcd22bacf8e5c28811`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 3.6 MB (3584945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35baff4c53633408e9b106331996c17d2435a9f86223ccf66af4d744ab9d01d3`  
		Last Modified: Sat, 19 Mar 2022 17:47:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdd7e19187739aa2f362a59e2d915dcaa59b335e67bdd353551c67bb90ced8`  
		Last Modified: Sat, 19 Mar 2022 17:47:53 GMT  
		Size: 2.3 MB (2273204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813bfa8c4c6e6c26ea2a87ebdb675a174456506a5d0aa737d1e4ea531b411e36`  
		Last Modified: Sat, 19 Mar 2022 17:47:50 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fe98b3cc0ebb249d658f7095bb9c125bb9d6efed76f7168ee105a0169ae26b`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9c19436dd2a8aac0006fc33f1cd9cb4c74e3b176b989903dedb71d396ff93`  
		Last Modified: Sat, 19 Mar 2022 17:48:35 GMT  
		Size: 88.7 MB (88741773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac0168aeb9a405897cad3f6229d56a3d1e2daa8a88ef338ceeb5c627d2ad90`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec17c09c0a08e85d66da1c0d38d5f8942d3e3904d45906de820ff0aa392ee79`  
		Last Modified: Sat, 19 Mar 2022 17:48:20 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:68e9c3d4d5c66588c498f1c3bd8d59e185b2ad28868ec2a8bffbcdedada1ab4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125724149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126b4633b52e1bc23b34961359e69be8b385283a15c4738c31f4b675a2dd4bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:47:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 15:47:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:15 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 15:47:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 15:47:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 15:47:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:47:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 15:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 15:49:00 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:00 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 15:49:01 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:02 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 15:49:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 15:49:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 15:49:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 15:49:26 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 15:49:28 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 15:49:29 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 15:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 15:49:30 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 15:49:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231508c81ce9a7932e8c0b10c046e86a3b3e040a3123739fc1deda47cf3174c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8a3e6a01e8993af537b2e08e2d7833d1c70d1aed7128d3a8c1e13f83241c7f`  
		Last Modified: Sat, 19 Mar 2022 15:55:29 GMT  
		Size: 5.3 MB (5320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6e0bbe4d4dff3b2a3b5137ff230f3662d027a3de5719061ba971cec1337ba`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 3.4 MB (3370387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729c491744da29835f5de3e588c8747d03891d83474ed38c5cc704bb44ad556`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b345ca8fc060929fdb17f7eab8eb5812a85de50aceb58c8a110fdcae2c6e00`  
		Last Modified: Sat, 19 Mar 2022 15:55:28 GMT  
		Size: 2.2 MB (2203907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ca4ff93e848f5a7f4c30849d48dac0dcaf0d5c5c960310f2f0fc815003a9`  
		Last Modified: Sat, 19 Mar 2022 15:55:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e4e5684ccfe111d173bc5c339ac3e2c7e268bb781b7ec626cb491d5733c6c1`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea715b3325269beb77618babf08f413a07a02c9360d20b66b8307e3e8beeb57b`  
		Last Modified: Sat, 19 Mar 2022 15:56:13 GMT  
		Size: 87.6 MB (87644820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ad829bad37000040993ce84153b347f26e484fe0a7dd03c8a4afd845ee1bd`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd6c8ad0863e4e3659a74806f93b47f0a5ab6027433133b576f981b2d8e4e4`  
		Last Modified: Sat, 19 Mar 2022 15:55:59 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:717064c331c4323a6b3beac591eb8e83ed9e26ead10f7b25b6703f9addad1190
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139539869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20dc38223bb008feffdd4824e11a9bee9295f851d7d34331d145346a9921dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Sat, 19 Mar 2022 21:09:36 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Sat, 19 Mar 2022 21:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 21:09:39 GMT
EXPOSE 3306
# Sat, 19 Mar 2022 21:09:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde08674f15819fa15d09618a7cf60cafb9f7c2595be4bcd3cf2470871c66b30`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:d45ff0e61a82b88b3fad76f3e67ecd7fad0994fb4904ead6320b4a11f63f04a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127723294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfdb12530dc6921555f000ba71620d69ec5e13054f4cf693f7cd1f0b25bbad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:32:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 17:32:58 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:32:59 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 17:33:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 17:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 17:33:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:33:15 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Mar 2022 17:33:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 18 Mar 2022 17:34:23 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:23 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 18 Mar 2022 17:34:24 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 18 Mar 2022 17:34:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 18 Mar 2022 17:34:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Mar 2022 17:34:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 18 Mar 2022 17:34:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 18 Mar 2022 17:34:47 GMT
COPY file:c7a0bb01c3d4445e83fe05cb40eb9923abf37a2e6271db38569e4829d49d6d38 in /usr/local/bin/ 
# Fri, 18 Mar 2022 17:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 17:34:48 GMT
EXPOSE 3306
# Fri, 18 Mar 2022 17:34:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f54a66b8b67360191aaf7739c7ae8d84e18554d06717ca00e5148cec84801`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59555044381768ae8c9d0dcb893379d7ee6d286d24389eeed759b6ca82a8b640`  
		Last Modified: Fri, 18 Mar 2022 17:36:55 GMT  
		Size: 5.4 MB (5378543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69441eb43595a26c16863744e5f301b9e2e0026272597a1208a2af43498d0ffd`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e32fbfb51530b430aaca1cf01b169559d0188f8eb4329f1f8720c5094e82f`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775c753ab577d326cf2268de9dc4301ba11a68f393fa351b4dfc95fc58e1792`  
		Last Modified: Fri, 18 Mar 2022 17:36:54 GMT  
		Size: 2.2 MB (2185813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf83c727602dd82b971ae3ac1af6f08540e00f2f0cb99dfd38ec6692307bf5`  
		Last Modified: Fri, 18 Mar 2022 17:36:53 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da9659e39b50233c80c276f702e4a191c6aa529487b3a0eba9c2d55f76142`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061117969687fd80688aa9e244cfd9ffd1a2c5f69f96a8645efa6c84a9c1429d`  
		Last Modified: Fri, 18 Mar 2022 17:37:30 GMT  
		Size: 89.8 MB (89815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e5a62b8d0e67eede1babf51b0fb97223c99d1481797241846ee885f4487fe`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2807f46ee5e63f640c4934a5de17c9692d862f0107079abbd31536ef9909d4`  
		Last Modified: Fri, 18 Mar 2022 17:37:17 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
