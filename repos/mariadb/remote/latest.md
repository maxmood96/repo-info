## `mariadb:latest`

```console
$ docker pull mariadb@sha256:86af37cc254e5d588861cfe704c1b51897ed12babba73c331b88f90a1b51811d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:be0069ebc09c00f5ff0b1900c5df05eb201cc01d3df4ab7828d26d38fae81654
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125585067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a348a04a8159339ed3ca053ea925f854252e6a6c3df6fa82c17625d1026f18b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:17:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 25 Nov 2020 23:17:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:17:30 GMT
ENV GOSU_VERSION=1.12
# Wed, 25 Nov 2020 23:17:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 25 Nov 2020 23:17:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 25 Nov 2020 23:17:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:17:55 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 25 Nov 2020 23:17:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 25 Nov 2020 23:17:58 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 25 Nov 2020 23:17:58 GMT
ENV MARIADB_VERSION=1:10.5.8+maria~focal
# Wed, 25 Nov 2020 23:18:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 25 Nov 2020 23:18:40 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 25 Nov 2020 23:18:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 25 Nov 2020 23:18:41 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Wed, 25 Nov 2020 23:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 23:18:41 GMT
EXPOSE 3306
# Wed, 25 Nov 2020 23:18:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22776aa82430af24b71cc0294b9c2bddd7c9f4a0213d13967e3bccc4f1296948`  
		Last Modified: Wed, 25 Nov 2020 23:22:26 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e64230d63d996dc81a927a75ec71730d7bb1ece4e43d64d6f2b830dab4bc82`  
		Last Modified: Wed, 25 Nov 2020 23:22:28 GMT  
		Size: 5.5 MB (5488627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30861f14a103eb6617d70c0b3ddb21d08ac133ed9d4e073f16e6b17a089d539`  
		Last Modified: Wed, 25 Nov 2020 23:22:26 GMT  
		Size: 1.3 MB (1324655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9e6a3da2446ca697e0ccb0d7c44012e8573d4eb708b36f11a876657970d7b`  
		Last Modified: Wed, 25 Nov 2020 23:22:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420a23f08c4147516e0f33d70c17c7f4d7a1e1ae4db8deb2a6a703f2c565483a`  
		Last Modified: Wed, 25 Nov 2020 23:22:25 GMT  
		Size: 1.3 MB (1267437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73f23de4821d5ddc74bdc29ed54ccafac21587e18baf11431413d7906c4371`  
		Last Modified: Wed, 25 Nov 2020 23:22:25 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8690a3260b734a0e2fe29912f283112edfc4aa22a31bf7282282726e993a8cc`  
		Last Modified: Wed, 25 Nov 2020 23:22:24 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202ba90333a4d33b3cdeeefcac43e219ea015f484b4b92e14f865621128e237`  
		Last Modified: Wed, 25 Nov 2020 23:22:42 GMT  
		Size: 88.9 MB (88930464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f860b4aa6bf9c5c6f3949001e39c976ac2eddf08295ab842bdc34114ac910`  
		Last Modified: Wed, 25 Nov 2020 23:22:24 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c892a2d0194f19d0aa29fa165cdbfeb6be619cbf68b7a9f715369f7f08c05311
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123207507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3ab601101c5c8e7e2238bb43637af4113de1d73fea960e84f06a91663ad364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:39:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 21 Jan 2021 05:39:52 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:39:53 GMT
ENV GOSU_VERSION=1.12
# Thu, 21 Jan 2021 05:40:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Jan 2021 05:40:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 05:40:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:40:24 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 21 Jan 2021 05:40:26 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 21 Jan 2021 05:40:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 21 Jan 2021 05:40:28 GMT
ENV MARIADB_VERSION=1:10.5.8+maria~focal
# Thu, 21 Jan 2021 05:40:29 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 21 Jan 2021 05:41:03 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 21 Jan 2021 05:41:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Jan 2021 05:41:06 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Thu, 21 Jan 2021 05:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:41:07 GMT
EXPOSE 3306
# Thu, 21 Jan 2021 05:41:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4b7d6f5e8d5e6798d5a292864880dff365e2942d95376ff609c1e916988569`  
		Last Modified: Thu, 21 Jan 2021 05:47:08 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a4309d7b0e4d6fd55d9f0e73656707ec9113fa99dd583b3935275c6cace298`  
		Last Modified: Thu, 21 Jan 2021 05:47:10 GMT  
		Size: 5.5 MB (5456508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947f6df950e3176936d1b2ce059122ae077f90f154470e287d5a63f97255590`  
		Last Modified: Thu, 21 Jan 2021 05:47:09 GMT  
		Size: 1.3 MB (1261886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875e2be5d265eb66b81430a94ae317145292da3e8f462c8212d22228522e5005`  
		Last Modified: Thu, 21 Jan 2021 05:47:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223795b422204535226226d07a28f273d181d1a8e10968fcfaff86965fef309e`  
		Last Modified: Thu, 21 Jan 2021 05:47:05 GMT  
		Size: 1.3 MB (1270864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc657677ae3e0889cf4b2d2f583ae2afff1e044699f2ef9efa09e3c11f3b6a`  
		Last Modified: Thu, 21 Jan 2021 05:47:05 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b09912c33f2e7b6a76320f2c201590899ee9b65c0a74c459e877702bbed84f`  
		Last Modified: Thu, 21 Jan 2021 05:47:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bd2c4c297c8d6742d93d7dcd7fa909f85e44eb27209214b362fc52f48a1d48`  
		Last Modified: Thu, 21 Jan 2021 05:47:29 GMT  
		Size: 88.0 MB (88034645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c6e38659e4a0759fb2b50eb8fa140f50e1abdc8038bb5cb07209c908d80fca`  
		Last Modified: Thu, 21 Jan 2021 05:47:05 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4ec60486a2aefc0d281a16c0113bde3927ac303f9d2975c0b22a0be7f67a6290
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135586735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a4737836fdb536b7942108344b1393db28f8019e87fdebd289251d3bacc79c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 25 Nov 2020 22:22:45 GMT
ADD file:349669e872fc8d76ff551a3eb05bb336a7d13ef8d99dc4f7604d54fc263a1a40 in / 
# Wed, 25 Nov 2020 22:23:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:23:19 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:23:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:23:34 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:51:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 26 Nov 2020 01:53:21 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:53:24 GMT
ENV GOSU_VERSION=1.12
# Thu, 26 Nov 2020 01:54:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 Nov 2020 01:54:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 26 Nov 2020 01:55:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:55:29 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 26 Nov 2020 01:55:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 26 Nov 2020 01:55:47 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 26 Nov 2020 01:55:51 GMT
ENV MARIADB_VERSION=1:10.5.8+maria~focal
# Thu, 26 Nov 2020 01:56:00 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 26 Nov 2020 01:59:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 26 Nov 2020 01:59:33 GMT
VOLUME [/var/lib/mysql]
# Thu, 26 Nov 2020 01:59:35 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Thu, 26 Nov 2020 01:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Nov 2020 01:59:42 GMT
EXPOSE 3306
# Thu, 26 Nov 2020 01:59:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0162c086f3047a91e0409b0f80e741887de3c5e5490b9be62d74a5c054c7d6b0`  
		Last Modified: Mon, 09 Nov 2020 19:03:51 GMT  
		Size: 33.3 MB (33278639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61108ece12882b4998d113ea62b7f4d286877fef610d4aae5b2d2f17d68bf8a4`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92bd8a59839464b3f3c73564e77cb7f1868ac3e96fcc07c1a77b85c51ba1b1`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69f85e3d602706866bb8a1ecd29e63d29a2a32244e9e7b47e3968fdd7c4108d`  
		Last Modified: Thu, 26 Nov 2020 02:31:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84920a54fef2502f206f9cb3b5bb1975352b385bac04144280cb60eb36db0050`  
		Last Modified: Thu, 26 Nov 2020 02:31:22 GMT  
		Size: 6.7 MB (6668651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d54f9080aa3ad0bb476c43e7fcf9b69b8fe1167e6d3cfe6536930f4da1994b`  
		Last Modified: Thu, 26 Nov 2020 02:31:21 GMT  
		Size: 1.2 MB (1244235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008fb86441f7ce445755c7032da78c37dd56307d3d8971d66ba0bbaa335bf5c5`  
		Last Modified: Thu, 26 Nov 2020 02:31:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944a2812cb2f46dbb5e5dce049a7852f551af023b9b27e6b3f20fe993bdfe75`  
		Last Modified: Thu, 26 Nov 2020 02:31:16 GMT  
		Size: 1.3 MB (1276561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c7c388f468c6270937b4b9d82f4f75e54ba4da8e2656383f2fc221cb5be7db`  
		Last Modified: Thu, 26 Nov 2020 02:31:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bb30a63ac97129cf522cac0ea14e9f7316f0f015036dc0914c9538c4feb8ad`  
		Last Modified: Thu, 26 Nov 2020 02:31:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd5c471121c347e0c8b586f07ea2e89d875f14a43614badf4de97b270cfc0a3`  
		Last Modified: Thu, 26 Nov 2020 02:31:37 GMT  
		Size: 93.1 MB (93107953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74a32f9efa1022b505f7893a1a320b8c9250bd87d191ec825e0895f65973118`  
		Last Modified: Thu, 26 Nov 2020 02:31:15 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
