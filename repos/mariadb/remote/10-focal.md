## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:16b58e1c775e3379a1d7eb303d3f6eb5c813bca07224f712dc10b0aba9ee015c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

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
