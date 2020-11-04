## `mariadb:focal`

```console
$ docker pull mariadb@sha256:2960a3d1ddb35dd454066b45005b4f694e18af76648833f1b9d93ab90cee7cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:3f18ce9e12e3ece07029895336f5497eeb2d9cb8fe148cc54d4905f77cbc062d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127800451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3986d60f138825865a5c22e19d877f0318d60e88383a0e2fb8baa05bd5a461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:33 GMT
ADD file:435d9776fdd3a1834f344fb82e459dbbb67cd50c71ab5e29b719273888d5bb7c in / 
# Fri, 23 Oct 2020 17:32:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:36 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:39:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 23 Oct 2020 18:39:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:39:41 GMT
ENV GOSU_VERSION=1.12
# Fri, 23 Oct 2020 18:39:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 23 Oct 2020 18:39:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 23 Oct 2020 18:39:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:39:56 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 23 Oct 2020 18:39:56 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 23 Oct 2020 18:39:57 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 04 Nov 2020 20:24:02 GMT
ENV MARIADB_VERSION=1:10.5.7+maria~focal
# Wed, 04 Nov 2020 20:24:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 04 Nov 2020 20:24:44 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Nov 2020 20:24:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Nov 2020 20:24:44 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Wed, 04 Nov 2020 20:24:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Nov 2020 20:24:45 GMT
EXPOSE 3306
# Wed, 04 Nov 2020 20:24:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6a5697faee43339ef8e33e3839060252392ad99325a48f7c9d7e93c22db4d4cf`  
		Last Modified: Thu, 08 Oct 2020 15:19:51 GMT  
		Size: 28.6 MB (28558714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba13d3bc422b493440f97a8f148d245e1999cb616cb05876edc3ef29e79852f2`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a254829d9e55168306fd80a49e02eb015551facee9c444d9dce3b26d19238b82`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee2cadd29fc000a7b2888c7747f65c9c91b93297d49a8ea9a964485590c6d0b`  
		Last Modified: Fri, 23 Oct 2020 18:42:20 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6915a184049d227be2aef7ba33041f9c24f9d493f3bee8f9ecadc1ec57ba3fd0`  
		Last Modified: Fri, 23 Oct 2020 18:42:21 GMT  
		Size: 5.5 MB (5488792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca6ffdb5f568bf70f64f6b023f1455225e79b582918cfc2d48c28b2a6c50dee`  
		Last Modified: Fri, 23 Oct 2020 18:42:20 GMT  
		Size: 1.3 MB (1324317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1537f7bbef8b1f078de10c272e534dd1e624ff50df83cc11510cecefb8e70437`  
		Last Modified: Fri, 23 Oct 2020 18:42:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790e54322d1411fb4d46c6a3f7540c8288e3afce665373833cbb02b0721c3d3`  
		Last Modified: Fri, 23 Oct 2020 18:42:18 GMT  
		Size: 1.3 MB (1266232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea98cb829471d5e7f3e03a0df8af7b7154f3c7fcf6941919962db75a3039a1fd`  
		Last Modified: Fri, 23 Oct 2020 18:42:17 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46bde67834a17e8ee971af5f4fdeca239d2e29d38bab8fd43b4e64f520a1393`  
		Last Modified: Wed, 04 Nov 2020 20:28:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78334cd64cf382a0908de6a6acb232aaee4857806021eb16769a2a2fed426c75`  
		Last Modified: Wed, 04 Nov 2020 20:29:58 GMT  
		Size: 91.2 MB (91151792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffdad591cf65da9285d7d78a3ccad9a25c904626051a406130a81136d364208`  
		Last Modified: Wed, 04 Nov 2020 20:28:25 GMT  
		Size: 4.9 KB (4922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c871924e98bcf3b694bc965d18a35b106713e4df439950e097447e97f410d949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125342356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ebc2956992c16a4a3a4fc769f32b2b5e5f28422e303bfdf4c83ff7e9f42dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Oct 2020 18:19:38 GMT
ADD file:83fb716eb29f83f9e0ea0422f76e651689972d98764d3e19e4017bbd3fe9d6e4 in / 
# Fri, 23 Oct 2020 18:19:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:19:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:19:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:19:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 19:33:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 23 Oct 2020 19:34:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:34:14 GMT
ENV GOSU_VERSION=1.12
# Fri, 23 Oct 2020 19:34:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 23 Oct 2020 19:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 23 Oct 2020 19:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:34:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 23 Oct 2020 19:34:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 23 Oct 2020 19:34:48 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 04 Nov 2020 19:43:21 GMT
ENV MARIADB_VERSION=1:10.5.7+maria~focal
# Wed, 04 Nov 2020 19:43:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 04 Nov 2020 19:44:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Nov 2020 19:44:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Nov 2020 19:44:19 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Wed, 04 Nov 2020 19:44:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Nov 2020 19:44:21 GMT
EXPOSE 3306
# Wed, 04 Nov 2020 19:44:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:00f57adb053c38c53d0655dee1ba47ed4cbd78cade062cf0e00f4b9790c7ed36`  
		Last Modified: Thu, 08 Oct 2020 08:25:26 GMT  
		Size: 27.2 MB (27163834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235828e8d75b4f9129ec8b0a00d4e3f1c4d100eedb3f00696a2ec78862082f6`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b606b1b8abdd386d8de6d1ce374b4dcdd4f7bcb4d68db64f09c03520fa5bf5`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1c04936d96ea5c0317454491309061a9bbb71f304201beba9d2a84d70278c6`  
		Last Modified: Fri, 23 Oct 2020 19:38:48 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838094e6dc11e995240cf827f8ba4add82c55538799aa31d59b62833848b4a7f`  
		Last Modified: Fri, 23 Oct 2020 19:38:49 GMT  
		Size: 5.5 MB (5456163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d156fbd7c528b7c56c7aab3103cd246779fc21c2d0704f38d68cf9e0e24ce0ec`  
		Last Modified: Fri, 23 Oct 2020 19:38:47 GMT  
		Size: 1.3 MB (1261580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96338e63cb2211929a174adb8f3717e1a2a8819e52367fcca58513ccb068d867`  
		Last Modified: Fri, 23 Oct 2020 19:38:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072483a93c1f4fdd36a34d7ec0087b270002ffc4b396eb10a969609ed1364d58`  
		Last Modified: Fri, 23 Oct 2020 19:38:45 GMT  
		Size: 1.3 MB (1265714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708913510fbcb15b1b99d5e6f4069454c58d03a3065c6bc95bb8ab01af8390a5`  
		Last Modified: Fri, 23 Oct 2020 19:38:45 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67698c770598346b6c5ae46f52c300ff6ee633c28839f40279204f04a88c5262`  
		Last Modified: Wed, 04 Nov 2020 19:49:34 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a961de22575b6b06a464bf26f49422bab6e3b7bf5dd958b9c6e10694773116e0`  
		Last Modified: Wed, 04 Nov 2020 19:49:56 GMT  
		Size: 90.2 MB (90184382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd393f66e88fda78abe2d92a343bed6f39eb4088c6d31abd289e19bf66868a0`  
		Last Modified: Wed, 04 Nov 2020 19:49:35 GMT  
		Size: 4.9 KB (4920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6537880be612f686e57d056fcd0c4746aa0e57fb15f762a14d0a5ff7b1a407a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137899065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d86026bdad491492472a375e6fb28410075e98ae03d76a5398c2e0aa711ace4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Oct 2020 19:25:52 GMT
ADD file:b9c09681764b8697badc8139e82a30efeb353faf61258695d1cd3a843c4de6a8 in / 
# Fri, 23 Oct 2020 19:26:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:26:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:26:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:27:03 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 19:55:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 23 Oct 2020 19:58:32 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:58:41 GMT
ENV GOSU_VERSION=1.12
# Fri, 23 Oct 2020 20:00:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 23 Oct 2020 20:01:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 23 Oct 2020 20:01:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 20:02:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 23 Oct 2020 20:02:36 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 23 Oct 2020 20:02:43 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 04 Nov 2020 20:17:02 GMT
ENV MARIADB_VERSION=1:10.5.7+maria~focal
# Wed, 04 Nov 2020 20:17:24 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 04 Nov 2020 20:25:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Nov 2020 20:26:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Nov 2020 20:26:07 GMT
COPY file:ea9c4b6befdd0eb133ee54ae54d4237bcd96ac6ceb915a1044533c52e382ec53 in /usr/local/bin/ 
# Wed, 04 Nov 2020 20:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Nov 2020 20:26:23 GMT
EXPOSE 3306
# Wed, 04 Nov 2020 20:26:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:76ff736f6fb2d41940a6cbdeab4242e9a64ef7df99ee4f3d9fcb9ec67bfccfc6`  
		Last Modified: Mon, 12 Oct 2020 16:20:28 GMT  
		Size: 33.3 MB (33275528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3d354673d1251716a1ed9cc3460095ee31664859e23d7e616546a17d287728`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434fabf01a92cfd54e3ae6f5e3dc7a3837ac2199999f713fbdf5cb2c800324a2`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8d4d42dc304605f1e3308df16201cafdb993d4a53eb11c8865e444f603c85`  
		Last Modified: Fri, 23 Oct 2020 20:26:26 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86154d9082951c9b2d658939cd2ebb2acd95a4609822131d650df7c34b26de8d`  
		Last Modified: Fri, 23 Oct 2020 20:26:26 GMT  
		Size: 6.7 MB (6668872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4317eb498e78b7b1ab9b98604730dd23addd5877207fee2e29065cc2a597519`  
		Last Modified: Fri, 23 Oct 2020 20:26:27 GMT  
		Size: 1.2 MB (1244112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee0bfbaadf08c70669d0ad3554b95a987af156889225eb5d82186c4aed3870`  
		Last Modified: Fri, 23 Oct 2020 20:26:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417da7e19201985162a4accf079629ab39a993d10ef41725c420a47557f878b`  
		Last Modified: Fri, 23 Oct 2020 20:26:20 GMT  
		Size: 1.3 MB (1273805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a761192d0ae5dd38ad710f39b7965f2ddf2f289179c0643f1500ed08367122`  
		Last Modified: Fri, 23 Oct 2020 20:26:18 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6bee37512d54b0c6cfd7641a9ca2e7ed1d10c761c8453ba3302beb20d8e1c`  
		Last Modified: Wed, 04 Nov 2020 20:59:41 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572674f878c3b1b9ef4cb79777ebff3ceef93daed47e807b6e0fff163d2d2b2c`  
		Last Modified: Wed, 04 Nov 2020 21:00:01 GMT  
		Size: 95.4 MB (95426046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5ccf49fd906858b9479479b1c447f9bc899ecef13c3167543005338423a5e7`  
		Last Modified: Wed, 04 Nov 2020 20:59:41 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
