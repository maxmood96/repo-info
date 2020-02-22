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
