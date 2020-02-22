<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10.1`](#mariadb101)
-	[`mariadb:10.1.44`](#mariadb10144)
-	[`mariadb:10.1.44-bionic`](#mariadb10144-bionic)
-	[`mariadb:10.1-bionic`](#mariadb101-bionic)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2.31`](#mariadb10231)
-	[`mariadb:10.2.31-bionic`](#mariadb10231-bionic)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3.22`](#mariadb10322)
-	[`mariadb:10.3.22-bionic`](#mariadb10322-bionic)
-	[`mariadb:10.3-bionic`](#mariadb103-bionic)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4.12`](#mariadb10412)
-	[`mariadb:10.4.12-bionic`](#mariadb10412-bionic)
-	[`mariadb:10.4-bionic`](#mariadb104-bionic)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5.1`](#mariadb1051)
-	[`mariadb:10.5.1-bionic`](#mariadb1051-bionic)
-	[`mariadb:10.5-bionic`](#mariadb105-bionic)
-	[`mariadb:10-bionic`](#mariadb10-bionic)
-	[`mariadb:beta`](#mariadbbeta)
-	[`mariadb:beta-bionic`](#mariadbbeta-bionic)
-	[`mariadb:bionic`](#mariadbbionic)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1`

```console
$ docker pull mariadb@sha256:6e14eb8f5b89a2e049d072e846414a592e0b5e900be5f9c6e1bf84632977f18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1` - linux; amd64

```console
$ docker pull mariadb@sha256:a1a1ae0bcdf1dc4029618bcf50035ce2a59c47c472f8a33ba25f30344557e0f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112610214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e091bb98f3e8532cca02a3e578b4832188dc95d94801775398aadb71b24005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 23:55:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:56:26 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:56:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:56:27 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:56:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:56:28 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:56:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da863b053a911f4df8f58075e90f2bb2bf2d2fb21f5235176abed515b4dc7`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e5ee2529491e8a4e370ce2a4631f36e9e1e82dfd23253ae6f688f4ed87788b`  
		Last Modified: Fri, 21 Feb 2020 23:58:23 GMT  
		Size: 79.3 MB (79265044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c38d2b9cdb3634dc505c75b7d32ac31807e78e42c1f8de824b6a06ac38d5cd`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cf2c18390065841a4c265c7ea604e31ba6e28eb23e1474896dab8a344789e4`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4e27d83c60bbbcdaa0b43ed217a00fe16c18ea3f564391e9a45334ed67f1c89f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105248632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5cb1c4741607ded97261d0309cb1ec20457a565dbeff9d2c898e480e605291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 22:17:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:17:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:17:50 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:17:50 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:17:53 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:17:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675360ae76ad78ef35b380ba3cb054d8e97511a2e56aa0b6e71b979f08963041`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abc27665f0acd610d7bd043da0ba018e0c4f6e14d3e47fb752f5ea3a6f44e3`  
		Last Modified: Fri, 21 Feb 2020 22:21:04 GMT  
		Size: 75.3 MB (75331848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02b73dc933da2d2ae6b5224d2744eb38d1aaeccb395654016b059c40b14839`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf69467181ffcd3d30bd575324a802a116c20aa287d54a30ffe4b655bdd4f8`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:79081d463148c9aa852dfb21e42dc8717f09f4f30171e8acf1140860ca5c6182
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117644552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8715be70dc9b17829ef8f6cb8aaa34a5067232077bd670c64d0e4938bf293d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:26:16 GMT
ENV MARIADB_MAJOR=10.1
# Sat, 22 Feb 2020 00:26:17 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Sat, 22 Feb 2020 00:26:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:28:09 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:28:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:28:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:28:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:28:38 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:28:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9cfb13a293b56136909ecdb0b1f7615c139169e76488cd0dd79e78f799977`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3405261af9b5e711831fda1b3db9e11ae82f602b38dc2b514dba8497ae630e74`  
		Last Modified: Sat, 22 Feb 2020 00:32:15 GMT  
		Size: 79.8 MB (79799368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d152ffea8cd423abfe98092164982b8b0917481238e0f491bb07475faf25c05c`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b305c21ca19b81fafe8cc9ef5cdcc53d7f1f073a3fd866bbb55c3dbf2ebbf`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.44`

```console
$ docker pull mariadb@sha256:6e14eb8f5b89a2e049d072e846414a592e0b5e900be5f9c6e1bf84632977f18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.44` - linux; amd64

```console
$ docker pull mariadb@sha256:a1a1ae0bcdf1dc4029618bcf50035ce2a59c47c472f8a33ba25f30344557e0f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112610214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e091bb98f3e8532cca02a3e578b4832188dc95d94801775398aadb71b24005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 23:55:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:56:26 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:56:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:56:27 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:56:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:56:28 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:56:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da863b053a911f4df8f58075e90f2bb2bf2d2fb21f5235176abed515b4dc7`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e5ee2529491e8a4e370ce2a4631f36e9e1e82dfd23253ae6f688f4ed87788b`  
		Last Modified: Fri, 21 Feb 2020 23:58:23 GMT  
		Size: 79.3 MB (79265044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c38d2b9cdb3634dc505c75b7d32ac31807e78e42c1f8de824b6a06ac38d5cd`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cf2c18390065841a4c265c7ea604e31ba6e28eb23e1474896dab8a344789e4`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.44` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4e27d83c60bbbcdaa0b43ed217a00fe16c18ea3f564391e9a45334ed67f1c89f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105248632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5cb1c4741607ded97261d0309cb1ec20457a565dbeff9d2c898e480e605291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 22:17:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:17:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:17:50 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:17:50 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:17:53 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:17:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675360ae76ad78ef35b380ba3cb054d8e97511a2e56aa0b6e71b979f08963041`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abc27665f0acd610d7bd043da0ba018e0c4f6e14d3e47fb752f5ea3a6f44e3`  
		Last Modified: Fri, 21 Feb 2020 22:21:04 GMT  
		Size: 75.3 MB (75331848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02b73dc933da2d2ae6b5224d2744eb38d1aaeccb395654016b059c40b14839`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf69467181ffcd3d30bd575324a802a116c20aa287d54a30ffe4b655bdd4f8`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.44` - linux; ppc64le

```console
$ docker pull mariadb@sha256:79081d463148c9aa852dfb21e42dc8717f09f4f30171e8acf1140860ca5c6182
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117644552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8715be70dc9b17829ef8f6cb8aaa34a5067232077bd670c64d0e4938bf293d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:26:16 GMT
ENV MARIADB_MAJOR=10.1
# Sat, 22 Feb 2020 00:26:17 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Sat, 22 Feb 2020 00:26:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:28:09 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:28:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:28:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:28:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:28:38 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:28:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9cfb13a293b56136909ecdb0b1f7615c139169e76488cd0dd79e78f799977`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3405261af9b5e711831fda1b3db9e11ae82f602b38dc2b514dba8497ae630e74`  
		Last Modified: Sat, 22 Feb 2020 00:32:15 GMT  
		Size: 79.8 MB (79799368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d152ffea8cd423abfe98092164982b8b0917481238e0f491bb07475faf25c05c`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b305c21ca19b81fafe8cc9ef5cdcc53d7f1f073a3fd866bbb55c3dbf2ebbf`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.44-bionic`

```console
$ docker pull mariadb@sha256:6e14eb8f5b89a2e049d072e846414a592e0b5e900be5f9c6e1bf84632977f18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.44-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a1a1ae0bcdf1dc4029618bcf50035ce2a59c47c472f8a33ba25f30344557e0f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112610214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e091bb98f3e8532cca02a3e578b4832188dc95d94801775398aadb71b24005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 23:55:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:56:26 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:56:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:56:27 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:56:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:56:28 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:56:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da863b053a911f4df8f58075e90f2bb2bf2d2fb21f5235176abed515b4dc7`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e5ee2529491e8a4e370ce2a4631f36e9e1e82dfd23253ae6f688f4ed87788b`  
		Last Modified: Fri, 21 Feb 2020 23:58:23 GMT  
		Size: 79.3 MB (79265044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c38d2b9cdb3634dc505c75b7d32ac31807e78e42c1f8de824b6a06ac38d5cd`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cf2c18390065841a4c265c7ea604e31ba6e28eb23e1474896dab8a344789e4`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.44-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4e27d83c60bbbcdaa0b43ed217a00fe16c18ea3f564391e9a45334ed67f1c89f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105248632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5cb1c4741607ded97261d0309cb1ec20457a565dbeff9d2c898e480e605291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 22:17:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:17:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:17:50 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:17:50 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:17:53 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:17:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675360ae76ad78ef35b380ba3cb054d8e97511a2e56aa0b6e71b979f08963041`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abc27665f0acd610d7bd043da0ba018e0c4f6e14d3e47fb752f5ea3a6f44e3`  
		Last Modified: Fri, 21 Feb 2020 22:21:04 GMT  
		Size: 75.3 MB (75331848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02b73dc933da2d2ae6b5224d2744eb38d1aaeccb395654016b059c40b14839`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf69467181ffcd3d30bd575324a802a116c20aa287d54a30ffe4b655bdd4f8`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.44-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:79081d463148c9aa852dfb21e42dc8717f09f4f30171e8acf1140860ca5c6182
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117644552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8715be70dc9b17829ef8f6cb8aaa34a5067232077bd670c64d0e4938bf293d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:26:16 GMT
ENV MARIADB_MAJOR=10.1
# Sat, 22 Feb 2020 00:26:17 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Sat, 22 Feb 2020 00:26:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:28:09 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:28:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:28:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:28:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:28:38 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:28:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9cfb13a293b56136909ecdb0b1f7615c139169e76488cd0dd79e78f799977`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3405261af9b5e711831fda1b3db9e11ae82f602b38dc2b514dba8497ae630e74`  
		Last Modified: Sat, 22 Feb 2020 00:32:15 GMT  
		Size: 79.8 MB (79799368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d152ffea8cd423abfe98092164982b8b0917481238e0f491bb07475faf25c05c`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b305c21ca19b81fafe8cc9ef5cdcc53d7f1f073a3fd866bbb55c3dbf2ebbf`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1-bionic`

```console
$ docker pull mariadb@sha256:6e14eb8f5b89a2e049d072e846414a592e0b5e900be5f9c6e1bf84632977f18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a1a1ae0bcdf1dc4029618bcf50035ce2a59c47c472f8a33ba25f30344557e0f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112610214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e091bb98f3e8532cca02a3e578b4832188dc95d94801775398aadb71b24005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 23:55:54 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 23:55:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:56:26 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:56:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:56:27 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:56:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:56:28 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:56:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da863b053a911f4df8f58075e90f2bb2bf2d2fb21f5235176abed515b4dc7`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e5ee2529491e8a4e370ce2a4631f36e9e1e82dfd23253ae6f688f4ed87788b`  
		Last Modified: Fri, 21 Feb 2020 23:58:23 GMT  
		Size: 79.3 MB (79265044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c38d2b9cdb3634dc505c75b7d32ac31807e78e42c1f8de824b6a06ac38d5cd`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cf2c18390065841a4c265c7ea604e31ba6e28eb23e1474896dab8a344789e4`  
		Last Modified: Fri, 21 Feb 2020 23:58:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4e27d83c60bbbcdaa0b43ed217a00fe16c18ea3f564391e9a45334ed67f1c89f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105248632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5cb1c4741607ded97261d0309cb1ec20457a565dbeff9d2c898e480e605291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_MAJOR=10.1
# Fri, 21 Feb 2020 22:16:58 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Fri, 21 Feb 2020 22:17:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:17:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:17:50 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:17:50 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:17:53 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:17:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675360ae76ad78ef35b380ba3cb054d8e97511a2e56aa0b6e71b979f08963041`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abc27665f0acd610d7bd043da0ba018e0c4f6e14d3e47fb752f5ea3a6f44e3`  
		Last Modified: Fri, 21 Feb 2020 22:21:04 GMT  
		Size: 75.3 MB (75331848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02b73dc933da2d2ae6b5224d2744eb38d1aaeccb395654016b059c40b14839`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf69467181ffcd3d30bd575324a802a116c20aa287d54a30ffe4b655bdd4f8`  
		Last Modified: Fri, 21 Feb 2020 22:20:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:79081d463148c9aa852dfb21e42dc8717f09f4f30171e8acf1140860ca5c6182
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117644552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8715be70dc9b17829ef8f6cb8aaa34a5067232077bd670c64d0e4938bf293d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:26:16 GMT
ENV MARIADB_MAJOR=10.1
# Sat, 22 Feb 2020 00:26:17 GMT
ENV MARIADB_VERSION=1:10.1.44+maria-1~bionic
# Sat, 22 Feb 2020 00:26:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:28:09 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:28:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:28:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:28:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:28:38 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:28:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9cfb13a293b56136909ecdb0b1f7615c139169e76488cd0dd79e78f799977`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3405261af9b5e711831fda1b3db9e11ae82f602b38dc2b514dba8497ae630e74`  
		Last Modified: Sat, 22 Feb 2020 00:32:15 GMT  
		Size: 79.8 MB (79799368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d152ffea8cd423abfe98092164982b8b0917481238e0f491bb07475faf25c05c`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b305c21ca19b81fafe8cc9ef5cdcc53d7f1f073a3fd866bbb55c3dbf2ebbf`  
		Last Modified: Sat, 22 Feb 2020 00:31:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:447c20d3ca6a4c91bad29a4792d9825abf856f984b23d66f654852cf7cd757d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:88fa9bb8c2c7d3a9426550abd0ad3fdc3958f30a2da632b0e6967f0a6d164a4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108441186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744dff8f3b648d0341376d0598730bbfff85c415c4666fb377b170b3f3aa19bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 23:55:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:46 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:47 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f02160cbe7f2700ac3f9e294e0d3565af9ae835a3008f8ca6e99f73769ad5`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff6f6782beab3708d2fd1d671843e3be32b546af02ac4cba207569fe2aee07`  
		Last Modified: Fri, 21 Feb 2020 23:57:59 GMT  
		Size: 75.1 MB (75096016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aaa59164dc5b8a34a03e8e0b171f8773afebf1858b133464b75a2e4707e5bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:46 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80005e6a2b2a4d603c8aff2ec14f62f7dcf92eeea3b1501887c534e31ec6587e`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a35944916683124c63b229291cb8fb845a76e00e521a3de7662a41ee2d8ad1c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103695000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dda625d87cfb568fade02fa43e835a3dbd68335e8a1a2febb2f4079b497fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 22:15:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:16:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:16:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:16:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:16:52 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6b002b110128afd7e2b50f5907a1db2e5035851e55118dca41ccedad155a9c`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c1f7827c7ea13e7ebd32d8f905c20d378fbb7be8047ab67a86c4402f8633e`  
		Last Modified: Fri, 21 Feb 2020 22:20:30 GMT  
		Size: 73.8 MB (73778219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f4923d9e3def7439efec7ae5158f5e6456eb8bed93594542cc16abacb2d984`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc8d5600c65554924b7e0fec1355ec2efe8c83d65f910c1c4d2720fbb1edd9`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:69cf5d70526dd37c27e2e7614fb7bfbcd080dd86dbf06242d2b0c3acc62c92cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115890311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7958261d36a27eacf012cc4de7779f37c7937e3809262567a68088cfd64d29e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:24:03 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 22 Feb 2020 00:24:05 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Sat, 22 Feb 2020 00:24:11 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:25:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:25:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:25:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:25:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:26:02 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:26:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839928690d42f83d7da90dc9b4885154743ea3370109bf9ebe24b38e74827f80`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0e2f9633afeba52742e34647c371c3bab2d4750ad715875211dfc03589e1`  
		Last Modified: Sat, 22 Feb 2020 00:31:39 GMT  
		Size: 78.0 MB (78045129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f677d4e05bf03452ff2db25aaf7915c6246c27a394f370c8bc306bef18bf09a2`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959bae9f2ed209cd2a96c37208a79a3c44235c488e2157c600e38b9098a6bb97`  
		Last Modified: Sat, 22 Feb 2020 00:31:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.31`

```console
$ docker pull mariadb@sha256:447c20d3ca6a4c91bad29a4792d9825abf856f984b23d66f654852cf7cd757d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.31` - linux; amd64

```console
$ docker pull mariadb@sha256:88fa9bb8c2c7d3a9426550abd0ad3fdc3958f30a2da632b0e6967f0a6d164a4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108441186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744dff8f3b648d0341376d0598730bbfff85c415c4666fb377b170b3f3aa19bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 23:55:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:46 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:47 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f02160cbe7f2700ac3f9e294e0d3565af9ae835a3008f8ca6e99f73769ad5`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff6f6782beab3708d2fd1d671843e3be32b546af02ac4cba207569fe2aee07`  
		Last Modified: Fri, 21 Feb 2020 23:57:59 GMT  
		Size: 75.1 MB (75096016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aaa59164dc5b8a34a03e8e0b171f8773afebf1858b133464b75a2e4707e5bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:46 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80005e6a2b2a4d603c8aff2ec14f62f7dcf92eeea3b1501887c534e31ec6587e`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.31` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a35944916683124c63b229291cb8fb845a76e00e521a3de7662a41ee2d8ad1c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103695000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dda625d87cfb568fade02fa43e835a3dbd68335e8a1a2febb2f4079b497fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 22:15:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:16:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:16:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:16:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:16:52 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6b002b110128afd7e2b50f5907a1db2e5035851e55118dca41ccedad155a9c`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c1f7827c7ea13e7ebd32d8f905c20d378fbb7be8047ab67a86c4402f8633e`  
		Last Modified: Fri, 21 Feb 2020 22:20:30 GMT  
		Size: 73.8 MB (73778219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f4923d9e3def7439efec7ae5158f5e6456eb8bed93594542cc16abacb2d984`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc8d5600c65554924b7e0fec1355ec2efe8c83d65f910c1c4d2720fbb1edd9`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.31` - linux; ppc64le

```console
$ docker pull mariadb@sha256:69cf5d70526dd37c27e2e7614fb7bfbcd080dd86dbf06242d2b0c3acc62c92cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115890311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7958261d36a27eacf012cc4de7779f37c7937e3809262567a68088cfd64d29e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:24:03 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 22 Feb 2020 00:24:05 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Sat, 22 Feb 2020 00:24:11 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:25:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:25:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:25:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:25:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:26:02 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:26:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839928690d42f83d7da90dc9b4885154743ea3370109bf9ebe24b38e74827f80`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0e2f9633afeba52742e34647c371c3bab2d4750ad715875211dfc03589e1`  
		Last Modified: Sat, 22 Feb 2020 00:31:39 GMT  
		Size: 78.0 MB (78045129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f677d4e05bf03452ff2db25aaf7915c6246c27a394f370c8bc306bef18bf09a2`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959bae9f2ed209cd2a96c37208a79a3c44235c488e2157c600e38b9098a6bb97`  
		Last Modified: Sat, 22 Feb 2020 00:31:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.31-bionic`

```console
$ docker pull mariadb@sha256:447c20d3ca6a4c91bad29a4792d9825abf856f984b23d66f654852cf7cd757d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.31-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:88fa9bb8c2c7d3a9426550abd0ad3fdc3958f30a2da632b0e6967f0a6d164a4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108441186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744dff8f3b648d0341376d0598730bbfff85c415c4666fb377b170b3f3aa19bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 23:55:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:46 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:47 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f02160cbe7f2700ac3f9e294e0d3565af9ae835a3008f8ca6e99f73769ad5`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff6f6782beab3708d2fd1d671843e3be32b546af02ac4cba207569fe2aee07`  
		Last Modified: Fri, 21 Feb 2020 23:57:59 GMT  
		Size: 75.1 MB (75096016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aaa59164dc5b8a34a03e8e0b171f8773afebf1858b133464b75a2e4707e5bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:46 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80005e6a2b2a4d603c8aff2ec14f62f7dcf92eeea3b1501887c534e31ec6587e`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.31-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a35944916683124c63b229291cb8fb845a76e00e521a3de7662a41ee2d8ad1c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103695000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dda625d87cfb568fade02fa43e835a3dbd68335e8a1a2febb2f4079b497fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 22:15:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:16:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:16:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:16:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:16:52 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6b002b110128afd7e2b50f5907a1db2e5035851e55118dca41ccedad155a9c`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c1f7827c7ea13e7ebd32d8f905c20d378fbb7be8047ab67a86c4402f8633e`  
		Last Modified: Fri, 21 Feb 2020 22:20:30 GMT  
		Size: 73.8 MB (73778219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f4923d9e3def7439efec7ae5158f5e6456eb8bed93594542cc16abacb2d984`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc8d5600c65554924b7e0fec1355ec2efe8c83d65f910c1c4d2720fbb1edd9`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.31-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:69cf5d70526dd37c27e2e7614fb7bfbcd080dd86dbf06242d2b0c3acc62c92cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115890311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7958261d36a27eacf012cc4de7779f37c7937e3809262567a68088cfd64d29e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:24:03 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 22 Feb 2020 00:24:05 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Sat, 22 Feb 2020 00:24:11 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:25:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:25:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:25:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:25:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:26:02 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:26:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839928690d42f83d7da90dc9b4885154743ea3370109bf9ebe24b38e74827f80`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0e2f9633afeba52742e34647c371c3bab2d4750ad715875211dfc03589e1`  
		Last Modified: Sat, 22 Feb 2020 00:31:39 GMT  
		Size: 78.0 MB (78045129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f677d4e05bf03452ff2db25aaf7915c6246c27a394f370c8bc306bef18bf09a2`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959bae9f2ed209cd2a96c37208a79a3c44235c488e2157c600e38b9098a6bb97`  
		Last Modified: Sat, 22 Feb 2020 00:31:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:447c20d3ca6a4c91bad29a4792d9825abf856f984b23d66f654852cf7cd757d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:88fa9bb8c2c7d3a9426550abd0ad3fdc3958f30a2da632b0e6967f0a6d164a4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108441186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744dff8f3b648d0341376d0598730bbfff85c415c4666fb377b170b3f3aa19bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 23:55:21 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 23:55:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:45 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:46 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:47 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f02160cbe7f2700ac3f9e294e0d3565af9ae835a3008f8ca6e99f73769ad5`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff6f6782beab3708d2fd1d671843e3be32b546af02ac4cba207569fe2aee07`  
		Last Modified: Fri, 21 Feb 2020 23:57:59 GMT  
		Size: 75.1 MB (75096016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aaa59164dc5b8a34a03e8e0b171f8773afebf1858b133464b75a2e4707e5bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:46 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80005e6a2b2a4d603c8aff2ec14f62f7dcf92eeea3b1501887c534e31ec6587e`  
		Last Modified: Fri, 21 Feb 2020 23:57:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a35944916683124c63b229291cb8fb845a76e00e521a3de7662a41ee2d8ad1c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103695000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dda625d87cfb568fade02fa43e835a3dbd68335e8a1a2febb2f4079b497fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 21 Feb 2020 22:15:53 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Fri, 21 Feb 2020 22:15:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:16:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:16:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:16:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:16:52 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6b002b110128afd7e2b50f5907a1db2e5035851e55118dca41ccedad155a9c`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c1f7827c7ea13e7ebd32d8f905c20d378fbb7be8047ab67a86c4402f8633e`  
		Last Modified: Fri, 21 Feb 2020 22:20:30 GMT  
		Size: 73.8 MB (73778219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f4923d9e3def7439efec7ae5158f5e6456eb8bed93594542cc16abacb2d984`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc8d5600c65554924b7e0fec1355ec2efe8c83d65f910c1c4d2720fbb1edd9`  
		Last Modified: Fri, 21 Feb 2020 22:20:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:69cf5d70526dd37c27e2e7614fb7bfbcd080dd86dbf06242d2b0c3acc62c92cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115890311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7958261d36a27eacf012cc4de7779f37c7937e3809262567a68088cfd64d29e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:24:03 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 22 Feb 2020 00:24:05 GMT
ENV MARIADB_VERSION=1:10.2.31+maria~bionic
# Sat, 22 Feb 2020 00:24:11 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:25:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:25:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:25:49 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:25:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:26:02 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:26:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839928690d42f83d7da90dc9b4885154743ea3370109bf9ebe24b38e74827f80`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0e2f9633afeba52742e34647c371c3bab2d4750ad715875211dfc03589e1`  
		Last Modified: Sat, 22 Feb 2020 00:31:39 GMT  
		Size: 78.0 MB (78045129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f677d4e05bf03452ff2db25aaf7915c6246c27a394f370c8bc306bef18bf09a2`  
		Last Modified: Sat, 22 Feb 2020 00:31:20 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959bae9f2ed209cd2a96c37208a79a3c44235c488e2157c600e38b9098a6bb97`  
		Last Modified: Sat, 22 Feb 2020 00:31:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:8cf4676590b73569cd1b4426f07cea522a4884a7b46342a3e61e3aa89b423f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:30cca32a30b6fa504fe3311b62c13410590b21a8b74768789f1a10073984e612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88f708652000380e4d8fb719c5fc5932d34a9aeedb3e13134cb8b447c0d85b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 23:54:49 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:17 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4607e8b05ffa3dc443b8d0e5b8260ed076bcac6c7ae8e6e2363614815e7164bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df878cd2aa70f5ea9be0ca9274271267f22439d4297ba8b6b02c1a50e9f50b`  
		Last Modified: Fri, 21 Feb 2020 23:57:40 GMT  
		Size: 76.1 MB (76123707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0c9086b840993c34d2c06df2b6a2df3d92c68a86f25b1b043dc4a287329f2`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e882546d78b7812ea41de7c5e351e846b8a0dbaaebc01f8959f9729178e18c`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:04436f0d9cb86550c2dec1ac7c9a10ffc4f6cfc563e84ac443a638ea8bfe8c3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104705429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88777cbcaff0223ec0e983a5baac73e0feccfa307711baabab71132627f3f87e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:57 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 22:14:58 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 22:14:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:15:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:15:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:15:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:15:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:15:46 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:15:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250690e4ffaa1bb4550345c347bc0cf4f6f13c9dc253226745244ae39964a05`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb7fb6be029e25ce3686cc63663bee0bd395f5bf422947ea53dd7df54dd5efa`  
		Last Modified: Fri, 21 Feb 2020 22:19:56 GMT  
		Size: 74.8 MB (74788645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e36e1a60b0cfc53b950ddf8b332565f676c3e235c47b4e422c54b7bb6cc91f`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 4.7 KB (4721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39736485b94ca33c3eb4dee0c341af991ee33f3e4e9ce43fc33e059d364afdac`  
		Last Modified: Fri, 21 Feb 2020 22:19:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9eee0ce5c5921be1a2e9cb86e915539b280594ce4ba762b31db57602155d3124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f6b108f9fa8b9669e5b29ea8118959ad3be8e1dddc52be7af63b4cc1a4e5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:21:37 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 22 Feb 2020 00:21:39 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Sat, 22 Feb 2020 00:21:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:23:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:23:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:23:34 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:23:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:23:46 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:23:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62b00105e246f35e5ca53af3365bca2a5717c6a62fd2bd0bf8219d4b78da6c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e31061754166d631812706a4f9093f407654ebf350a235b86a6ff29f694060`  
		Last Modified: Sat, 22 Feb 2020 00:31:02 GMT  
		Size: 79.1 MB (79144891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b91424baf92e32c59e0ffe4118efd34331cf5f65421fc9bcfecdc9329db25c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba3f3e5284c6c1a2c1c42635c6674e5b6a8945cc3d43fc5a502f4081099deed`  
		Last Modified: Sat, 22 Feb 2020 00:30:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.22`

```console
$ docker pull mariadb@sha256:8cf4676590b73569cd1b4426f07cea522a4884a7b46342a3e61e3aa89b423f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.22` - linux; amd64

```console
$ docker pull mariadb@sha256:30cca32a30b6fa504fe3311b62c13410590b21a8b74768789f1a10073984e612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88f708652000380e4d8fb719c5fc5932d34a9aeedb3e13134cb8b447c0d85b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 23:54:49 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:17 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4607e8b05ffa3dc443b8d0e5b8260ed076bcac6c7ae8e6e2363614815e7164bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df878cd2aa70f5ea9be0ca9274271267f22439d4297ba8b6b02c1a50e9f50b`  
		Last Modified: Fri, 21 Feb 2020 23:57:40 GMT  
		Size: 76.1 MB (76123707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0c9086b840993c34d2c06df2b6a2df3d92c68a86f25b1b043dc4a287329f2`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e882546d78b7812ea41de7c5e351e846b8a0dbaaebc01f8959f9729178e18c`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.22` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:04436f0d9cb86550c2dec1ac7c9a10ffc4f6cfc563e84ac443a638ea8bfe8c3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104705429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88777cbcaff0223ec0e983a5baac73e0feccfa307711baabab71132627f3f87e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:57 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 22:14:58 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 22:14:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:15:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:15:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:15:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:15:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:15:46 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:15:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250690e4ffaa1bb4550345c347bc0cf4f6f13c9dc253226745244ae39964a05`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb7fb6be029e25ce3686cc63663bee0bd395f5bf422947ea53dd7df54dd5efa`  
		Last Modified: Fri, 21 Feb 2020 22:19:56 GMT  
		Size: 74.8 MB (74788645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e36e1a60b0cfc53b950ddf8b332565f676c3e235c47b4e422c54b7bb6cc91f`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 4.7 KB (4721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39736485b94ca33c3eb4dee0c341af991ee33f3e4e9ce43fc33e059d364afdac`  
		Last Modified: Fri, 21 Feb 2020 22:19:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.22` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9eee0ce5c5921be1a2e9cb86e915539b280594ce4ba762b31db57602155d3124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f6b108f9fa8b9669e5b29ea8118959ad3be8e1dddc52be7af63b4cc1a4e5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:21:37 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 22 Feb 2020 00:21:39 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Sat, 22 Feb 2020 00:21:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:23:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:23:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:23:34 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:23:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:23:46 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:23:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62b00105e246f35e5ca53af3365bca2a5717c6a62fd2bd0bf8219d4b78da6c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e31061754166d631812706a4f9093f407654ebf350a235b86a6ff29f694060`  
		Last Modified: Sat, 22 Feb 2020 00:31:02 GMT  
		Size: 79.1 MB (79144891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b91424baf92e32c59e0ffe4118efd34331cf5f65421fc9bcfecdc9329db25c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba3f3e5284c6c1a2c1c42635c6674e5b6a8945cc3d43fc5a502f4081099deed`  
		Last Modified: Sat, 22 Feb 2020 00:30:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.22-bionic`

```console
$ docker pull mariadb@sha256:8cf4676590b73569cd1b4426f07cea522a4884a7b46342a3e61e3aa89b423f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.22-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:30cca32a30b6fa504fe3311b62c13410590b21a8b74768789f1a10073984e612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88f708652000380e4d8fb719c5fc5932d34a9aeedb3e13134cb8b447c0d85b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 23:54:49 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:17 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4607e8b05ffa3dc443b8d0e5b8260ed076bcac6c7ae8e6e2363614815e7164bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df878cd2aa70f5ea9be0ca9274271267f22439d4297ba8b6b02c1a50e9f50b`  
		Last Modified: Fri, 21 Feb 2020 23:57:40 GMT  
		Size: 76.1 MB (76123707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0c9086b840993c34d2c06df2b6a2df3d92c68a86f25b1b043dc4a287329f2`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e882546d78b7812ea41de7c5e351e846b8a0dbaaebc01f8959f9729178e18c`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.22-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:04436f0d9cb86550c2dec1ac7c9a10ffc4f6cfc563e84ac443a638ea8bfe8c3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104705429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88777cbcaff0223ec0e983a5baac73e0feccfa307711baabab71132627f3f87e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:57 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 22:14:58 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 22:14:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:15:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:15:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:15:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:15:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:15:46 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:15:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250690e4ffaa1bb4550345c347bc0cf4f6f13c9dc253226745244ae39964a05`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb7fb6be029e25ce3686cc63663bee0bd395f5bf422947ea53dd7df54dd5efa`  
		Last Modified: Fri, 21 Feb 2020 22:19:56 GMT  
		Size: 74.8 MB (74788645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e36e1a60b0cfc53b950ddf8b332565f676c3e235c47b4e422c54b7bb6cc91f`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 4.7 KB (4721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39736485b94ca33c3eb4dee0c341af991ee33f3e4e9ce43fc33e059d364afdac`  
		Last Modified: Fri, 21 Feb 2020 22:19:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.22-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9eee0ce5c5921be1a2e9cb86e915539b280594ce4ba762b31db57602155d3124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f6b108f9fa8b9669e5b29ea8118959ad3be8e1dddc52be7af63b4cc1a4e5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:21:37 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 22 Feb 2020 00:21:39 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Sat, 22 Feb 2020 00:21:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:23:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:23:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:23:34 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:23:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:23:46 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:23:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62b00105e246f35e5ca53af3365bca2a5717c6a62fd2bd0bf8219d4b78da6c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e31061754166d631812706a4f9093f407654ebf350a235b86a6ff29f694060`  
		Last Modified: Sat, 22 Feb 2020 00:31:02 GMT  
		Size: 79.1 MB (79144891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b91424baf92e32c59e0ffe4118efd34331cf5f65421fc9bcfecdc9329db25c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba3f3e5284c6c1a2c1c42635c6674e5b6a8945cc3d43fc5a502f4081099deed`  
		Last Modified: Sat, 22 Feb 2020 00:30:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-bionic`

```console
$ docker pull mariadb@sha256:8cf4676590b73569cd1b4426f07cea522a4884a7b46342a3e61e3aa89b423f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:30cca32a30b6fa504fe3311b62c13410590b21a8b74768789f1a10073984e612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88f708652000380e4d8fb719c5fc5932d34a9aeedb3e13134cb8b447c0d85b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 23:54:48 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 23:54:49 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:55:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:55:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:55:16 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:55:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:55:17 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:55:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4607e8b05ffa3dc443b8d0e5b8260ed076bcac6c7ae8e6e2363614815e7164bd`  
		Last Modified: Fri, 21 Feb 2020 23:57:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df878cd2aa70f5ea9be0ca9274271267f22439d4297ba8b6b02c1a50e9f50b`  
		Last Modified: Fri, 21 Feb 2020 23:57:40 GMT  
		Size: 76.1 MB (76123707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0c9086b840993c34d2c06df2b6a2df3d92c68a86f25b1b043dc4a287329f2`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e882546d78b7812ea41de7c5e351e846b8a0dbaaebc01f8959f9729178e18c`  
		Last Modified: Fri, 21 Feb 2020 23:57:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:04436f0d9cb86550c2dec1ac7c9a10ffc4f6cfc563e84ac443a638ea8bfe8c3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104705429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88777cbcaff0223ec0e983a5baac73e0feccfa307711baabab71132627f3f87e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:57 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 21 Feb 2020 22:14:58 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Fri, 21 Feb 2020 22:14:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:15:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:15:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:15:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:15:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:15:46 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:15:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250690e4ffaa1bb4550345c347bc0cf4f6f13c9dc253226745244ae39964a05`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb7fb6be029e25ce3686cc63663bee0bd395f5bf422947ea53dd7df54dd5efa`  
		Last Modified: Fri, 21 Feb 2020 22:19:56 GMT  
		Size: 74.8 MB (74788645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e36e1a60b0cfc53b950ddf8b332565f676c3e235c47b4e422c54b7bb6cc91f`  
		Last Modified: Fri, 21 Feb 2020 22:19:34 GMT  
		Size: 4.7 KB (4721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39736485b94ca33c3eb4dee0c341af991ee33f3e4e9ce43fc33e059d364afdac`  
		Last Modified: Fri, 21 Feb 2020 22:19:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9eee0ce5c5921be1a2e9cb86e915539b280594ce4ba762b31db57602155d3124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f6b108f9fa8b9669e5b29ea8118959ad3be8e1dddc52be7af63b4cc1a4e5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:21:37 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 22 Feb 2020 00:21:39 GMT
ENV MARIADB_VERSION=1:10.3.22+maria~bionic
# Sat, 22 Feb 2020 00:21:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:23:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:23:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:23:34 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:23:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:23:46 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:23:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62b00105e246f35e5ca53af3365bca2a5717c6a62fd2bd0bf8219d4b78da6c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e31061754166d631812706a4f9093f407654ebf350a235b86a6ff29f694060`  
		Last Modified: Sat, 22 Feb 2020 00:31:02 GMT  
		Size: 79.1 MB (79144891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b91424baf92e32c59e0ffe4118efd34331cf5f65421fc9bcfecdc9329db25c`  
		Last Modified: Sat, 22 Feb 2020 00:30:44 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba3f3e5284c6c1a2c1c42635c6674e5b6a8945cc3d43fc5a502f4081099deed`  
		Last Modified: Sat, 22 Feb 2020 00:30:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.12`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.12` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.12` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.12` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.12-bionic`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.12-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.12-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.12-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-bionic`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.1`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.1` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.1-bionic`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-bionic`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-bionic`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta-bionic`

```console
$ docker pull mariadb@sha256:6da40b2db998b88b98f27f451cbe041f667ca5c0010f9ee7cbefedae98d35878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:a966fa4b0773e6ed67bfdd6af0d3ed7dc940226f219da18e16505ff3033fa5fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113610010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0faecd25b199f6c8cae044c415babe05e924dcd5bae16f78568418cfef900d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 23:53:47 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 23:53:48 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:15 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba57875199a40b8a6e80236fbed16ebde3cf152ee991971920dc2a69b02313a`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7531599e7b78e97020d007cbc56b5a4aab0b9ac6cdf144c0e401339edd81c1`  
		Last Modified: Fri, 21 Feb 2020 23:56:55 GMT  
		Size: 80.3 MB (80264958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30167b82874ad3876874e808c08ea58893ffe9bb8b4bd8c5101ce5eaf5f4821c`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:07e1ea78cb608fb4d384537d851aa76acad243c9b8caacde3bb83401a953323a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108828216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ce0a18d62c8cd46cd8e2ed8f2589e52b3e5dafbf268d744dadd20895233bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 21 Feb 2020 22:13:10 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Fri, 21 Feb 2020 22:13:12 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:13:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:13:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:13:54 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:13:55 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:13:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab89257f4c196669238fa44e68a705e97a2c7c9459dfd9618e749d7a0db24`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8f13c9181f09bed05dcd51509be5cc9902172cba9ad62482566576ffca6969`  
		Last Modified: Fri, 21 Feb 2020 22:18:39 GMT  
		Size: 78.9 MB (78911556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d433311485e62bafa5e32fc83b85584bdf1b69fb6ce603d99dca23a01f1935`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eea240a5d1ddabe99777a27323547acefb3250e5abacd0f1303f460a5bc3817a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3cecd80c48ae1a2260f1bb2150584df22c4cf23d62189f1cdf9a5d92b4d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:16:16 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 22 Feb 2020 00:16:19 GMT
ENV MARIADB_VERSION=1:10.5.1+maria~bionic
# Sat, 22 Feb 2020 00:16:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:18:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:18:33 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:18:36 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:18:49 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf4696cbdade6ef57cc3abb645b70bf568ae454c933222d1339c8e5ad76799`  
		Last Modified: Sat, 22 Feb 2020 00:29:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783f06cf48732ab9730ffbafbe3bde66010252c9b14b81c9b568e93db75ad8a`  
		Last Modified: Sat, 22 Feb 2020 00:29:32 GMT  
		Size: 83.5 MB (83453488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93161794276efaf9a6b2cdea5b567b922a40711d3e3b4805683b5ea20a41f7d0`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:bionic`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:05b8bf8e3c5cefddb6e7190ff8a5e720872728a9f6b27e5e90a16ebe984091c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:b3116f425f51353e2ba71b04647977b035c2c578d276e2d4285bd2798e8199ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113361879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e8f717676870bb9b3fdeee8be5d025a7d80819b4b9c87febc7e2e6fe6458e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:53:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 23:53:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:30 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 23:53:39 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 23:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 23:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:53:46 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 23:53:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 23:54:20 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 23:54:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 23:54:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 23:54:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 23:54:41 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 23:54:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 23:54:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 23:54:42 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 23:54:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b41ae57cefb62971c2193d693d1c32c793f417d01b45c56fe6c4679902a4ac0`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd5cacc3700199eee00a4d88f2e2bb277aab4fe9428afcda1f2a4a0b2fc637`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 4.8 MB (4807015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f96ac6b2583b79cd23f6cad78c95be3ca6be1cd283b910f3dea921f392fe357`  
		Last Modified: Fri, 21 Feb 2020 23:56:43 GMT  
		Size: 867.6 KB (867619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224e6c8f8410746d647e1e3514a4383ecc3022e09d54e53890e3a0dfcb2e2ca`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc4c2808be6ea9fd2946556461489bbd6603242938ea0fc917548b48208c93`  
		Last Modified: Fri, 21 Feb 2020 23:56:41 GMT  
		Size: 929.9 KB (929879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae8752de58b09b1ee0d996ec65bb97bac3e20e18b0dfa3572a89ea0a90e939`  
		Last Modified: Fri, 21 Feb 2020 23:56:40 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adda6a0eec54373e5061eea579be359bc0c3d142bfc4f23e4b049d78b41d09b`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b660834848d2be27d338ee8c320f9f1f8fe2179759ac8df06658c78d85c1b8`  
		Last Modified: Fri, 21 Feb 2020 23:57:16 GMT  
		Size: 80.0 MB (80016708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac908ac8219c33ea8a87021faf90c16cf1cfad1f2bee630ab472dadd325b162`  
		Last Modified: Fri, 21 Feb 2020 23:57:03 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62be07fe3c17cf59d6779391fab8bf6273d3ad98a308df89fd32704eced89cf7`  
		Last Modified: Fri, 21 Feb 2020 23:57:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:319f5b1d4d92d0c6c8215e279f5e67a15af58632ebcc03744adc5198497d8746
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108608223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cf3e810dd8253cabcfd364334b66d8438be110f0bb0eb1d75fdee46130547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:12:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 21 Feb 2020 22:12:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:12:36 GMT
ENV GOSU_VERSION=1.10
# Fri, 21 Feb 2020 22:12:54 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 21 Feb 2020 22:12:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:13:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 21 Feb 2020 22:13:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:14:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 21 Feb 2020 22:14:03 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Fri, 21 Feb 2020 22:14:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 21 Feb 2020 22:14:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 21 Feb 2020 22:14:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Feb 2020 22:14:42 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:14:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 22:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:14:45 GMT
EXPOSE 3306
# Fri, 21 Feb 2020 22:14:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32448d74b93e8687953d8261c385c052e507419876df11b0275ad06c44aadf9c`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06700188e3ceb7527907f30f04f58bc4b3524142fc8a78a8742c57b104c4a7f9`  
		Last Modified: Fri, 21 Feb 2020 22:18:20 GMT  
		Size: 4.4 MB (4392351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e6bc6b906cdae9f42697f6e6c16c276a11857c943c3852c430b3965e02163`  
		Last Modified: Fri, 21 Feb 2020 22:18:19 GMT  
		Size: 833.9 KB (833893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499dec95886a159ac0f33a4d620e3b62faacb486b71cb4007e691bb61635f2e`  
		Last Modified: Fri, 21 Feb 2020 22:18:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfc101c0ecc207fcaaca12b55b9caf16b1db8e36c1bd24437ff888f28e8501b`  
		Last Modified: Fri, 21 Feb 2020 22:18:17 GMT  
		Size: 920.9 KB (920937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fdc04685bbb093edf0f207f9dde97850a9aa01c86535dd2e7852066c08163`  
		Last Modified: Fri, 21 Feb 2020 22:18:16 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c9b232eff2439f45e648d52b75f3b7eb86c6e41cf961f3487426fcb1f52c72`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac20251802bdf47498a8047858e5f7ddc8556ac09e2867fe2eba86b284aac`  
		Last Modified: Fri, 21 Feb 2020 22:19:18 GMT  
		Size: 78.7 MB (78691443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e241d11070e8cfbb380b459c7caca52b891c6ac2ecd94e00fe7a4a77b5c16d2`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ab64296260c6b129b92c433ba88c346c1f46bdb6efa25e36fc2741b69e350`  
		Last Modified: Fri, 21 Feb 2020 22:18:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:574b8fbd1139ab062b50e6669e480a2b3b3b62cea5a25362c086e40aed01aeec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121067391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07494469266b5db85add1f6c80a6edfb7a772128fd40c625cc8812d8a5b4c3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:13:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 22 Feb 2020 00:14:38 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:14:43 GMT
ENV GOSU_VERSION=1.10
# Sat, 22 Feb 2020 00:15:29 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 22 Feb 2020 00:15:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 00:16:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:16:07 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 22 Feb 2020 00:16:14 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 00:19:11 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 22 Feb 2020 00:19:14 GMT
ENV MARIADB_VERSION=1:10.4.12+maria~bionic
# Sat, 22 Feb 2020 00:19:20 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 22 Feb 2020 00:21:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 22 Feb 2020 00:21:11 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Feb 2020 00:21:14 GMT
COPY file:b50ad8ff787b4cfa95592fcec7d18449b174968f9d6a562653cbe39fe9022863 in /usr/local/bin/ 
# Sat, 22 Feb 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 22 Feb 2020 00:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 00:21:26 GMT
EXPOSE 3306
# Sat, 22 Feb 2020 00:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ce08603b7ef3127e3ac4a2e63fed37ec9a6e5ef67247bf7bbb50eadd18cbd`  
		Last Modified: Sat, 22 Feb 2020 00:29:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4b5e1a00ddd08901833be34c46365dd132fd5959d85eb8dc0e9b068e8cc4b`  
		Last Modified: Sat, 22 Feb 2020 00:29:18 GMT  
		Size: 5.6 MB (5627975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60430165b6a595ba7774beab6840c7af9e056c9119b84c490098f9c45a80d875`  
		Last Modified: Sat, 22 Feb 2020 00:29:17 GMT  
		Size: 836.0 KB (835980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38851a4d02e68112d39496088d9d4444d494e669fa5f3369f3e497c1e3a1db2`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2507042f257577147bc9c8edcde590e976b76df26b9b3ad59b8a7fcfbff3f3`  
		Last Modified: Sat, 22 Feb 2020 00:29:16 GMT  
		Size: 931.7 KB (931676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e4a09f2078de34182c41e4456097553b43ed2b3b9d1dcc33ad1de684fccb`  
		Last Modified: Sat, 22 Feb 2020 00:29:13 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b308ee98418b03025aa0f7478346d94a22522c15413ab5eb4be6c119fbe801f`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0129b630de23ba6c3ede8ea774fcb3c4ebc54d77465fab1fa5d546ec8a5`  
		Last Modified: Sat, 22 Feb 2020 00:30:14 GMT  
		Size: 83.2 MB (83222208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe998ada4103990c55692ab4022543d2ce968992e18e4fb18b2c6e72cb84c222`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac6089580988ca3fc8c95532596168c5d67f491f4185162110ed51f50dd54a4`  
		Last Modified: Sat, 22 Feb 2020 00:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
