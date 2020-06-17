<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10.1`](#mariadb101)
-	[`mariadb:10.1.45`](#mariadb10145)
-	[`mariadb:10.1.45-bionic`](#mariadb10145-bionic)
-	[`mariadb:10.1-bionic`](#mariadb101-bionic)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2.32`](#mariadb10232)
-	[`mariadb:10.2.32-bionic`](#mariadb10232-bionic)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3.23`](#mariadb10323)
-	[`mariadb:10.3.23-focal`](#mariadb10323-focal)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4.13`](#mariadb10413)
-	[`mariadb:10.4.13-focal`](#mariadb10413-focal)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5.3`](#mariadb1053)
-	[`mariadb:10.5.3-focal`](#mariadb1053-focal)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)
-	[`mariadb:rc`](#mariadbrc)
-	[`mariadb:rc-focal`](#mariadbrc-focal)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1`

```console
$ docker pull mariadb@sha256:e0a62c4b7ffeafca3c56355052562c8cd6f7ce00b3325bd4dcc8c056efd47a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:81163f01648de623a9b60b8cfd7ee8c88ceba03b57d78e697e5e2b92fa83bf19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105806431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bd07b6df0a30a6628356f571d47b31a2f342a5560bb96d49cb5cf08f6d823f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:17:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 17 Jun 2020 03:17:09 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 17 Jun 2020 03:17:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:18:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:18:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:18:25 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:18:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:18:32 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:18:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24864f1785e11f26df826dbca4381098ccbe2346d195fe46155f5fd155f980`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd58ebf837777464c0b04c0a22db70b1c7386bb543f8ca645c3f46766686ec50`  
		Last Modified: Wed, 17 Jun 2020 03:21:54 GMT  
		Size: 75.5 MB (75458042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05032ca75fa619de20fd23f4c970dd1188832b343b2c6997cbd7a81afd3b017f`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8898282f7d6722e05f3423109deb18843324791def2fd17ee3a8200d8b5d3317`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45`

```console
$ docker pull mariadb@sha256:e0a62c4b7ffeafca3c56355052562c8cd6f7ce00b3325bd4dcc8c056efd47a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:81163f01648de623a9b60b8cfd7ee8c88ceba03b57d78e697e5e2b92fa83bf19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105806431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bd07b6df0a30a6628356f571d47b31a2f342a5560bb96d49cb5cf08f6d823f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:17:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 17 Jun 2020 03:17:09 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 17 Jun 2020 03:17:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:18:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:18:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:18:25 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:18:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:18:32 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:18:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24864f1785e11f26df826dbca4381098ccbe2346d195fe46155f5fd155f980`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd58ebf837777464c0b04c0a22db70b1c7386bb543f8ca645c3f46766686ec50`  
		Last Modified: Wed, 17 Jun 2020 03:21:54 GMT  
		Size: 75.5 MB (75458042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05032ca75fa619de20fd23f4c970dd1188832b343b2c6997cbd7a81afd3b017f`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8898282f7d6722e05f3423109deb18843324791def2fd17ee3a8200d8b5d3317`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45-bionic`

```console
$ docker pull mariadb@sha256:e0a62c4b7ffeafca3c56355052562c8cd6f7ce00b3325bd4dcc8c056efd47a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:81163f01648de623a9b60b8cfd7ee8c88ceba03b57d78e697e5e2b92fa83bf19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105806431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bd07b6df0a30a6628356f571d47b31a2f342a5560bb96d49cb5cf08f6d823f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:17:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 17 Jun 2020 03:17:09 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 17 Jun 2020 03:17:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:18:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:18:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:18:25 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:18:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:18:32 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:18:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24864f1785e11f26df826dbca4381098ccbe2346d195fe46155f5fd155f980`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd58ebf837777464c0b04c0a22db70b1c7386bb543f8ca645c3f46766686ec50`  
		Last Modified: Wed, 17 Jun 2020 03:21:54 GMT  
		Size: 75.5 MB (75458042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05032ca75fa619de20fd23f4c970dd1188832b343b2c6997cbd7a81afd3b017f`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8898282f7d6722e05f3423109deb18843324791def2fd17ee3a8200d8b5d3317`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1-bionic`

```console
$ docker pull mariadb@sha256:e0a62c4b7ffeafca3c56355052562c8cd6f7ce00b3325bd4dcc8c056efd47a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:f5d667508a4e81b80e16a17e4992069cc51275f3b89f99e08d2ce977ee8309db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad20783a626b1fe3239b83ea2bc12842cbab5929696a13c52a7e4d7f7d3c1e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:10:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 20:51:55 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 20:51:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:52:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:52:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:50 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:51 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4846a5211cc19dffa385f6714141c9e4065ea1b8272f2d1b588919011e3bd`  
		Last Modified: Wed, 13 May 2020 21:44:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708c0ebee78df6312129e0d725d9170751f26045dadf8a29d284a923fe4aa4f`  
		Last Modified: Wed, 13 May 2020 21:44:48 GMT  
		Size: 79.4 MB (79386150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6485241d1dd9a47ea4347f8c032f9900c3fcc01b13802f80428807c69edda7a`  
		Last Modified: Fri, 29 May 2020 00:22:34 GMT  
		Size: 4.8 KB (4848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab70faee57e501347812c3016018fdb049c752cc1352f893deecea9950b218`  
		Last Modified: Fri, 29 May 2020 00:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:81163f01648de623a9b60b8cfd7ee8c88ceba03b57d78e697e5e2b92fa83bf19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105806431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bd07b6df0a30a6628356f571d47b31a2f342a5560bb96d49cb5cf08f6d823f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:17:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 17 Jun 2020 03:17:09 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 17 Jun 2020 03:17:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:18:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:18:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:18:25 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:18:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:18:32 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:18:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24864f1785e11f26df826dbca4381098ccbe2346d195fe46155f5fd155f980`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd58ebf837777464c0b04c0a22db70b1c7386bb543f8ca645c3f46766686ec50`  
		Last Modified: Wed, 17 Jun 2020 03:21:54 GMT  
		Size: 75.5 MB (75458042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05032ca75fa619de20fd23f4c970dd1188832b343b2c6997cbd7a81afd3b017f`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8898282f7d6722e05f3423109deb18843324791def2fd17ee3a8200d8b5d3317`  
		Last Modified: Wed, 17 Jun 2020 03:21:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85e25546584603d8decb3fe84f4f278753887cfa8e00949394e686b0f64bfb04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eea4aa235dc181ba3d212c6f42b0477f587cae986ea50d2d75d261588a06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:12:55 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 13 May 2020 21:31:40 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Wed, 13 May 2020 21:31:45 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:33:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:33:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:19:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:19:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:19:26 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:19:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17121903157faf437d6a4f6226aedb91205bbbb4fe4716d7701dfcdede225d`  
		Last Modified: Wed, 13 May 2020 21:39:21 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3a841d422b4bcc462480b87ddbfcb3b42dba96389f930c4b97da6ed5c0e6b`  
		Last Modified: Wed, 13 May 2020 21:40:05 GMT  
		Size: 79.9 MB (79937498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dfdeed66ae409ce46eda9a632a3039fad2a639aa54c0edd3efa1ce8c2b2037`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d9aec94715e1d14f6608baaee3dec819d3b3900f25264fd029f31c88133b7`  
		Last Modified: Fri, 29 May 2020 00:21:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:f812cd3b239156a11104862004b5963f8ba19ca376235cfce2b24d81e2efe76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b2d6bab568674b5a2d0cf86fa063ee8d6c1c54dcf21b8491b989f3b9e7be0953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6cda706c76533371c4abdef5c354f58c1d38bb2cf9cf595efc1641eff3ca36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:16:00 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 17 Jun 2020 03:16:01 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 17 Jun 2020 03:16:05 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:16:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:16:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:16:53 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:16:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:16:57 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:16:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516051e9db2c1eaedd7b32f5e3af19570092a8e0de4c2ffc520ca53eb7c11d32`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db261243a4047e9ba71fb73d2478600a5e7c5a14fe2cfb58d9a62580b6d4f8a`  
		Last Modified: Wed, 17 Jun 2020 03:21:23 GMT  
		Size: 73.7 MB (73732793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ee56fb785c7f07292d1bf14dfbbc5287aefc198f563c71894e0abe49f12a7`  
		Last Modified: Wed, 17 Jun 2020 03:20:58 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92065b440d508e489da250e9108dec8386f865678971f4ca8d80685b425bab47`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32`

```console
$ docker pull mariadb@sha256:f812cd3b239156a11104862004b5963f8ba19ca376235cfce2b24d81e2efe76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b2d6bab568674b5a2d0cf86fa063ee8d6c1c54dcf21b8491b989f3b9e7be0953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6cda706c76533371c4abdef5c354f58c1d38bb2cf9cf595efc1641eff3ca36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:16:00 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 17 Jun 2020 03:16:01 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 17 Jun 2020 03:16:05 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:16:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:16:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:16:53 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:16:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:16:57 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:16:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516051e9db2c1eaedd7b32f5e3af19570092a8e0de4c2ffc520ca53eb7c11d32`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db261243a4047e9ba71fb73d2478600a5e7c5a14fe2cfb58d9a62580b6d4f8a`  
		Last Modified: Wed, 17 Jun 2020 03:21:23 GMT  
		Size: 73.7 MB (73732793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ee56fb785c7f07292d1bf14dfbbc5287aefc198f563c71894e0abe49f12a7`  
		Last Modified: Wed, 17 Jun 2020 03:20:58 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92065b440d508e489da250e9108dec8386f865678971f4ca8d80685b425bab47`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32-bionic`

```console
$ docker pull mariadb@sha256:f812cd3b239156a11104862004b5963f8ba19ca376235cfce2b24d81e2efe76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b2d6bab568674b5a2d0cf86fa063ee8d6c1c54dcf21b8491b989f3b9e7be0953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6cda706c76533371c4abdef5c354f58c1d38bb2cf9cf595efc1641eff3ca36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:16:00 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 17 Jun 2020 03:16:01 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 17 Jun 2020 03:16:05 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:16:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:16:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:16:53 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:16:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:16:57 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:16:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516051e9db2c1eaedd7b32f5e3af19570092a8e0de4c2ffc520ca53eb7c11d32`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db261243a4047e9ba71fb73d2478600a5e7c5a14fe2cfb58d9a62580b6d4f8a`  
		Last Modified: Wed, 17 Jun 2020 03:21:23 GMT  
		Size: 73.7 MB (73732793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ee56fb785c7f07292d1bf14dfbbc5287aefc198f563c71894e0abe49f12a7`  
		Last Modified: Wed, 17 Jun 2020 03:20:58 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92065b440d508e489da250e9108dec8386f865678971f4ca8d80685b425bab47`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:f812cd3b239156a11104862004b5963f8ba19ca376235cfce2b24d81e2efe76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:eb1f6c4a4a01985d20283423421817c1a201e85de1192c6bed681dfee3664af3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108996232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a144d514f6729156a6491a1806310f5e2d93042b24d921d8ba4bca7fc5e979c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:07:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 20:07:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:25 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 20:07:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 20:07:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 20:07:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:07:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 20:07:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 20:09:29 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 20:51:21 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 20:51:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 20:51:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 20:51:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:21:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:21:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:21:46 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:21:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69dcc78e96eb792fb67240a5ff4db2c3e3cb1ff55f97df2bddba0706fb5f6e6`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222f44c5392d7a36df5eb58bb790223d332bd187fc56f006ecd66ad762f740e8`  
		Last Modified: Fri, 24 Apr 2020 20:10:59 GMT  
		Size: 4.8 MB (4807438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc64ea97b9cf087977c9a7972347db33f40487bcdd29abb41e7acf4c265335a`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 1.3 MB (1326271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912a149de6b3da2628c28ecfbd75992cda34df498d3634e6145bfdf1832a1a2`  
		Last Modified: Fri, 24 Apr 2020 20:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6cf5b569752da3539a3b0c377a2a4f64e90f26eb7c89d405cf0168c923106`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 929.2 KB (929212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05be3688e04bf9961d4912e2dd86ff9832e72ec8c6b2d34c053e87ccf991a6`  
		Last Modified: Fri, 24 Apr 2020 20:10:57 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1edf2a8459b3c38e04a5cdabd6030f22e09bb2f653d0e57020e1e77b530ea`  
		Last Modified: Wed, 13 May 2020 21:44:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4954c91ebe442c8d5c4bbcfb190d71bc2adc03debcf88573e9d55e9abaf0e9`  
		Last Modified: Wed, 13 May 2020 21:44:25 GMT  
		Size: 75.2 MB (75194669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae91c8217271570b6c43609f856cee367ae34cf2106fb9a589bc7698e52ba11`  
		Last Modified: Fri, 29 May 2020 00:22:25 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec0680735c5ff37d37fa985b1970c8fa5d17887fb1d8f72e9cdb6310e8f20a`  
		Last Modified: Fri, 29 May 2020 00:22:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b2d6bab568674b5a2d0cf86fa063ee8d6c1c54dcf21b8491b989f3b9e7be0953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6cda706c76533371c4abdef5c354f58c1d38bb2cf9cf595efc1641eff3ca36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:14:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:15:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:15:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:15:54 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:15:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:16:00 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 17 Jun 2020 03:16:01 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 17 Jun 2020 03:16:05 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:16:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:16:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:16:53 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:16:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:16:57 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:16:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b68b27ee966b229ac43ed7048a671d2055a84a1a75255aab275a7ef0bee0a`  
		Last Modified: Wed, 17 Jun 2020 03:21:02 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dcf68c77759699edde8372b7806b3547ec70e4f9661b46839aea933744427`  
		Last Modified: Wed, 17 Jun 2020 03:21:03 GMT  
		Size: 4.4 MB (4393585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b07d6de4d5e23270179bd5b5bc987d6d07d71cc011afefdc924335fd892c6f`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 1.3 MB (1263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9493ccc4b8eabb44739c956a5c1e0909c4022f0dd7f4f13a2d93ea2be9f8b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e2cd62c3d72d3d5d38230ce5eba2f557162b9fe6b6cf5999af1ac4167d55b`  
		Last Modified: Wed, 17 Jun 2020 03:21:01 GMT  
		Size: 921.3 KB (921252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a15c8231b3505554cbacda6a6f2c3abdbecf485b3671785aecc5e62940c37`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516051e9db2c1eaedd7b32f5e3af19570092a8e0de4c2ffc520ca53eb7c11d32`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db261243a4047e9ba71fb73d2478600a5e7c5a14fe2cfb58d9a62580b6d4f8a`  
		Last Modified: Wed, 17 Jun 2020 03:21:23 GMT  
		Size: 73.7 MB (73732793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ee56fb785c7f07292d1bf14dfbbc5287aefc198f563c71894e0abe49f12a7`  
		Last Modified: Wed, 17 Jun 2020 03:20:58 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92065b440d508e489da250e9108dec8386f865678971f4ca8d80685b425bab47`  
		Last Modified: Wed, 17 Jun 2020 03:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5c36761b92100924e7ac536939ac4137c013ae05b8cdeee7b462a956d7bc80cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116238898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cecc321cebccae35ecb8359bb9daea184ed336e8226b517019f2218f1f9dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:56:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Apr 2020 11:57:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:58:10 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 11:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 11:59:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 11:59:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:59:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Apr 2020 11:59:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 12:09:45 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 May 2020 21:29:28 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Wed, 13 May 2020 21:29:36 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 May 2020 21:31:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 May 2020 21:31:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2020 00:18:34 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 29 May 2020 00:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 29 May 2020 00:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2020 00:18:49 GMT
EXPOSE 3306
# Fri, 29 May 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050ed2928ca970f92a55e32757c9a2bed2d12719ac1f8ffe473007ebfb5627a`  
		Last Modified: Fri, 24 Apr 2020 12:16:35 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f165cd342f0a2ae619a609d6874d38864a5cd9a56cdfc8876d139942c86b00b`  
		Last Modified: Fri, 24 Apr 2020 12:16:39 GMT  
		Size: 5.6 MB (5628683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783ab2db059c111e57346fcb3db7da7d24c0be81aad5b27e670d5f0d2340fd8`  
		Last Modified: Fri, 24 Apr 2020 12:16:34 GMT  
		Size: 1.2 MB (1246415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659f23141b0ba1d73e5c6f1922b480865fa378174eccf526a7280c40ad370d2`  
		Last Modified: Fri, 24 Apr 2020 12:16:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad047e312e9236cb8b8743456d6e073c71c56ffa4f21e1af8769ad6726c805`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 931.5 KB (931523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22944a8e89f53e83da58e8806dc3c4be25b3a2754635c108fc327c6ddb42789b`  
		Last Modified: Fri, 24 Apr 2020 12:16:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dfeebe25cc02ad3288ff3f03a92be19ef8664c7907b436859177684da5e508`  
		Last Modified: Wed, 13 May 2020 21:38:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145af634d57422884d13c0715874a0329aa049813e46d8a3ebace3333d997f67`  
		Last Modified: Wed, 13 May 2020 21:39:02 GMT  
		Size: 78.0 MB (77983227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a739aee0daaa14a73304a5a190b76705b8b2a5a6a3ff501b4b983bbcc2926f4`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b735d3acd167ca7325abc2eecd2cb3e3753090746bc73aada056882ff2b1`  
		Last Modified: Fri, 29 May 2020 00:21:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:9003bb57c01e19b490176cfe4acaf34f8129ee04f360f613215f58cd21fd2650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a69a4a8bccb9597b57f81643f559e3d1b2cee44bb215c204c2f5159a9ae97579
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b27062829add21ec8d0b3d74f1ef51bb4438a8518d20ca89f8d5e9374b5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:13:32 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 17 Jun 2020 03:13:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Wed, 17 Jun 2020 03:13:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:14:34 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:14:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:14:39 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:14:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:14:43 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:14:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445eca511b60e64d21f8207041fe54b9bd6617fc54718ba794f3175844979e11`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fec43af213a1bfc738753d2d1f4c41b0f3f1da2aa121d7b0763c3d8f57d2b0`  
		Last Modified: Wed, 17 Jun 2020 03:20:49 GMT  
		Size: 81.7 MB (81654023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986a44632e5b5abc044d6affb938f2c9dcb524c37b6cc67f2b4300c85729f48`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2252950723d5f17c46bf0c226adc423b8fd063cc31178e45ba2edd84f0631c`  
		Last Modified: Wed, 17 Jun 2020 03:20:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23`

```console
$ docker pull mariadb@sha256:9003bb57c01e19b490176cfe4acaf34f8129ee04f360f613215f58cd21fd2650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a69a4a8bccb9597b57f81643f559e3d1b2cee44bb215c204c2f5159a9ae97579
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b27062829add21ec8d0b3d74f1ef51bb4438a8518d20ca89f8d5e9374b5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:13:32 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 17 Jun 2020 03:13:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Wed, 17 Jun 2020 03:13:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:14:34 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:14:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:14:39 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:14:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:14:43 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:14:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445eca511b60e64d21f8207041fe54b9bd6617fc54718ba794f3175844979e11`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fec43af213a1bfc738753d2d1f4c41b0f3f1da2aa121d7b0763c3d8f57d2b0`  
		Last Modified: Wed, 17 Jun 2020 03:20:49 GMT  
		Size: 81.7 MB (81654023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986a44632e5b5abc044d6affb938f2c9dcb524c37b6cc67f2b4300c85729f48`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2252950723d5f17c46bf0c226adc423b8fd063cc31178e45ba2edd84f0631c`  
		Last Modified: Wed, 17 Jun 2020 03:20:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23-focal`

```console
$ docker pull mariadb@sha256:9003bb57c01e19b490176cfe4acaf34f8129ee04f360f613215f58cd21fd2650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a69a4a8bccb9597b57f81643f559e3d1b2cee44bb215c204c2f5159a9ae97579
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b27062829add21ec8d0b3d74f1ef51bb4438a8518d20ca89f8d5e9374b5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:13:32 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 17 Jun 2020 03:13:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Wed, 17 Jun 2020 03:13:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:14:34 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:14:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:14:39 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:14:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:14:43 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:14:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445eca511b60e64d21f8207041fe54b9bd6617fc54718ba794f3175844979e11`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fec43af213a1bfc738753d2d1f4c41b0f3f1da2aa121d7b0763c3d8f57d2b0`  
		Last Modified: Wed, 17 Jun 2020 03:20:49 GMT  
		Size: 81.7 MB (81654023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986a44632e5b5abc044d6affb938f2c9dcb524c37b6cc67f2b4300c85729f48`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2252950723d5f17c46bf0c226adc423b8fd063cc31178e45ba2edd84f0631c`  
		Last Modified: Wed, 17 Jun 2020 03:20:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:9003bb57c01e19b490176cfe4acaf34f8129ee04f360f613215f58cd21fd2650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:91436c443be256515804695e3e4bb10c63da53b874a24a5fa1fcc58a134d5f03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119186637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6eec5b8a160e797d9496acc941ad5862888dd3e9886c4025bc35a34d19c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 18:25:31 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 18:25:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:57 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:59 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c589be17d1ce856007eb81ff3b231e335f96a58eb63481253b453db7f6beaa`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64145edf74b26c97e82a91fdfb45dca3ce0bb054ec1ba9bb9fd8b591fe6e8d60`  
		Last Modified: Fri, 12 Jun 2020 18:27:31 GMT  
		Size: 82.5 MB (82510657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e760ac9383651d4f5e8d2d2b9952fe03f09e2754a5aa5c9a244dc9adbde1ba`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4a7d63a16d9790172e0fd5999a0c6a9a9ef2059def2b3b0b89020f42dbca7`  
		Last Modified: Fri, 12 Jun 2020 18:27:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a69a4a8bccb9597b57f81643f559e3d1b2cee44bb215c204c2f5159a9ae97579
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b27062829add21ec8d0b3d74f1ef51bb4438a8518d20ca89f8d5e9374b5aeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:13:32 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 17 Jun 2020 03:13:33 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Wed, 17 Jun 2020 03:13:35 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:14:34 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:14:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:14:39 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:14:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:14:43 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:14:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445eca511b60e64d21f8207041fe54b9bd6617fc54718ba794f3175844979e11`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fec43af213a1bfc738753d2d1f4c41b0f3f1da2aa121d7b0763c3d8f57d2b0`  
		Last Modified: Wed, 17 Jun 2020 03:20:49 GMT  
		Size: 81.7 MB (81654023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986a44632e5b5abc044d6affb938f2c9dcb524c37b6cc67f2b4300c85729f48`  
		Last Modified: Wed, 17 Jun 2020 03:20:22 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2252950723d5f17c46bf0c226adc423b8fd063cc31178e45ba2edd84f0631c`  
		Last Modified: Wed, 17 Jun 2020 03:20:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1df4e1ece3cc05b9beec65be935b9cca6ce678cedcd1874c0a2c22217a38eda4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a469296cf72ff7286030b3e5166c79524fa0703bb766a11f44b772b5ece0053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 19:04:51 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 12 Jun 2020 19:05:05 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Fri, 12 Jun 2020 19:05:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:11:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:11:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:11:27 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:11:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:12:00 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3e3684e96a3273ea708e45edce664e0bd43d8c982c92d03a51588c6a24eb0f`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10f969e78ca7b123018dc731e9a741d6561b2192e4089d101fe72f7449b088a`  
		Last Modified: Fri, 12 Jun 2020 19:15:12 GMT  
		Size: 86.5 MB (86537862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c80fc2592043d6d3771e008c7ae87e5b1b8b37765333729601521f21aeae90`  
		Last Modified: Fri, 12 Jun 2020 19:14:51 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6dbf7a2967109ac5529a53c507be0a0a24c7df5e1cbefd878f94ea6f6c6430`  
		Last Modified: Fri, 12 Jun 2020 19:14:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13-focal`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.3`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.3` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.3-focal`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:179ce92d0e91f93a5450c0082e7c2f4efa5bd12e428ea1d92b7231877b6a044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e4d56b012b5815eea3eb97e4a5fddc3af03a7fad57f6d260e8006ca6dd84191d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121141744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedee596baf898213b6c6fa3f6e85cdd241d4895929b4ee616f4fecb1b5fe32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:12:01 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 17 Jun 2020 03:12:03 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Wed, 17 Jun 2020 03:12:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:13:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:13:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:13:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Jun 2020 03:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:22 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:13:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712fe8380a5dab2812149815f9b4fcc767668ddc4643b37dc71b69fae13182f4`  
		Last Modified: Wed, 17 Jun 2020 03:19:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4e1609f9d47217958d6572c892741e53f3e8486cd6c3acc13979c0ac6617d`  
		Last Modified: Wed, 17 Jun 2020 03:20:06 GMT  
		Size: 86.0 MB (85958547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cf83f0eb1e53a8fb19e8426997512ae60184c2a2a8b9bd93c5641dd7e160`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a0037345701389ee78c0db3cb2d9aeb2a763d4d1b919f41d844215e4077a0`  
		Last Modified: Wed, 17 Jun 2020 03:19:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:rc`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:rc` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:rc-focal`

```console
$ docker pull mariadb@sha256:c9035aeb0e32d5402316297e7193569f3ae090424beafbadf9eb013516f57066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1c43c2c9a9cbc8d6d917b3baccc746029611401140afacbc341f9e0543f693d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125468046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d666ead09d0cdb6b38628b20884b7a034975d73e0c72bf72af995bf25b32ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:24:12 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:24:13 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:24:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:24:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:24:45 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:24:46 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:24:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a69879e3e44e2c33e196212dc1e1f81aa3f8a2f150e64ba2be5415cebf05f`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3434e5ff172ae3f9a2ebac367af66daecf7e55fb5d24d1202cc34d1a680d5a`  
		Last Modified: Fri, 12 Jun 2020 18:26:37 GMT  
		Size: 88.8 MB (88792188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9318b4b2608af288b8a860c61f31daa1e48322b0a4d0588a94e1ae7269bb89a9`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5d9530cad29b975d291f821eaebd49e6881acb9a8efc0423850354d90d744e1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123000524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3965045a55bb99785448c8a123400a5bca96d80068e34c26a8f3337b7610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:09:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 17 Jun 2020 03:10:06 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:07 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:10:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:42 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 17 Jun 2020 03:10:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:10:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 17 Jun 2020 03:10:51 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Wed, 17 Jun 2020 03:10:54 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 17 Jun 2020 03:11:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 17 Jun 2020 03:11:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 17 Jun 2020 03:11:44 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:11:46 GMT
EXPOSE 3306
# Wed, 17 Jun 2020 03:11:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4d3724fecce71f52b8a17f7ad9ebf162db52b783ef0d7d861b590223b335b9`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8393fb279f94da2864ee6a6c96cb99a1f2720eebfc2ba5c10cc0fe59b12c20`  
		Last Modified: Wed, 17 Jun 2020 03:18:57 GMT  
		Size: 5.5 MB (5457292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66da321c9b056392f2ad4b0d4649a0e2edfc19d36eb116e03ce76fb97f7f80`  
		Last Modified: Wed, 17 Jun 2020 03:18:56 GMT  
		Size: 1.3 MB (1259377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9eb8c45f57a14876d84cec78ec763db6ac07fc41baf222474d20ceaafa98c`  
		Last Modified: Wed, 17 Jun 2020 03:18:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e1362c2c73f0111db30ecfe0c55b569d3c0636aaf91d853cfb27098e3d0ff7`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 1.3 MB (1263702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ba076cb71a018cc18cea4c70f154c5d9b07003f213f0e1ed15c1685ef2b3c`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd60525ec7284bbc9031d96eb3dc6cd0315a6270d73258e140ffc0224913e1`  
		Last Modified: Wed, 17 Jun 2020 03:18:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d811a9fa6973046663b719b3be8568312ff1e2c6a2165bdca586bed13bd6c2`  
		Last Modified: Wed, 17 Jun 2020 03:19:19 GMT  
		Size: 87.8 MB (87817448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a759ae25216bdd1041318eec3cfa09273b46dfcca9e0a9aabee444077a0eb2b4`  
		Last Modified: Wed, 17 Jun 2020 03:18:54 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7f3c6e4fbe1d904fe0f1daf0b28dd7b6055906d0e4ef545e0f167305737edfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135491752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4482a6d35ab27dc6622588f472d707755fd0242ccf076f18f56b764f32d2f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:49:25 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 12 Jun 2020 18:49:36 GMT
ENV MARIADB_VERSION=1:10.5.3+maria~focal
# Fri, 12 Jun 2020 18:50:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:55:32 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:55:52 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:55:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:12 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c120bad3d45c4179d4a0c2dcde4937f90d39332c52fb866de70e4b7634460`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5768c1a14ad9b899134606bad0b1bf95337891f65101e352d91fe125d74a1e7`  
		Last Modified: Fri, 12 Jun 2020 19:13:37 GMT  
		Size: 93.0 MB (92981382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e462c378a4b7787721cd8cb5720e89d8e9696d398174bb7b4d6d60bacfada`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
