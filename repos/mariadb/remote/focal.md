## `mariadb:focal`

```console
$ docker pull mariadb@sha256:273369dddb8430bf5e46fb4ed163e83316f82ef2a05a9a5bea27cc7fbc7cdf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ed4b1285078871f1c699fde87299d7003e41cc17c1efd3808f85902b4e147da8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125580845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95867b5288692523149a43cf511b91dd180cd40dffd6b607bdaa5b8f03da00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:32 GMT
ADD file:65a1cc50a9867c153deb3bed36d9d51d469fb123df6ee0ba31e01646edf1a1c4 in / 
# Fri, 24 Jul 2020 14:38:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:59:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Jul 2020 16:59:50 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:59:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:59:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 17:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 17:00:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:00:09 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Jul 2020 17:00:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 17:00:10 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 11 Aug 2020 20:30:08 GMT
ENV MARIADB_VERSION=1:10.5.5+maria~focal
# Tue, 11 Aug 2020 20:30:09 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 11 Aug 2020 20:30:41 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 11 Aug 2020 20:30:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Aug 2020 20:30:42 GMT
COPY file:7a2bd14d0848358d403d6a9913bd5da8743de51ba46b60bf676d773828a634a0 in /usr/local/bin/ 
# Tue, 11 Aug 2020 20:30:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Aug 2020 20:30:42 GMT
EXPOSE 3306
# Tue, 11 Aug 2020 20:30:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3ff22d22a8554f746f90a78b501da38d56a46f2ddba0dfec8b260aebaa61b3ba`  
		Last Modified: Mon, 20 Jul 2020 15:20:12 GMT  
		Size: 28.6 MB (28557306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb79d19722c46b9c0829811d7a5a0ae82c8771ab7f2f68e7d3a3ed6bd5d5d0`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 32.3 KB (32320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323d0d660b6a7da8df08a01dbc7250f38cfa2161db00c7c27c0b20be07a8236a`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f616834fd07522cbfd33f0dfa848903599320b5c7191b59fe9aa7562f956a1`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ed0160f03e84d203a2bf929df74e2d0c69b5c5c5c865daaf434a98ef7f97ed`  
		Last Modified: Fri, 24 Jul 2020 17:04:33 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a122e9306ac4224d5707da113ebd6ddcafc9eb780e805970d0e82cf009f15620`  
		Last Modified: Fri, 24 Jul 2020 17:04:34 GMT  
		Size: 5.5 MB (5488252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673e89352b197e26f491f9031239315cf3f32cfd0da5b8ebd8a1c64e6f28a26d`  
		Last Modified: Fri, 24 Jul 2020 17:04:32 GMT  
		Size: 1.3 MB (1323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf1e694359bf26987ab04d447e4eeeee53ad382a9e4ca8eccd09a0ac9f93e75`  
		Last Modified: Fri, 24 Jul 2020 17:04:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f5e4f6ead334b03d2fd76e779412a232d7b1d8ea59e3c9ff0956dc6b085e9e`  
		Last Modified: Fri, 24 Jul 2020 17:04:31 GMT  
		Size: 1.3 MB (1265785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41772aadb3dfa07f462edb79e3a3a36d25775c2766c9e5ebfbc0340c2bac3f1`  
		Last Modified: Fri, 24 Jul 2020 17:04:31 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca25bbc109b2c30c9ae24f75488b6865ae4a00ba2611bdbc82f77e2e6665e772`  
		Last Modified: Tue, 11 Aug 2020 20:33:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff1f953b69b9b84fbe7d99b2dd28e6383035b79fee073158b5b2af60e3dc36`  
		Last Modified: Tue, 11 Aug 2020 20:34:01 GMT  
		Size: 88.9 MB (88902531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321435eb1c0c83e38a1667c997725997f55de069586027975e44d4ce43c464`  
		Last Modified: Tue, 11 Aug 2020 20:33:45 GMT  
		Size: 5.1 KB (5057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:625b748ab9c6834776532506563735f465ef5046350977a1c1296b4b4336b282
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123226285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878d41de3572b183d450fe7da4a3482b7afd3ccaf57adcf23773ad0a4d8ca448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Jul 2020 16:24:06 GMT
ADD file:26bd57f1dbcfd1a91715cc84cf0f221783655f16bbb7a912aaf20507cc252535 in / 
# Fri, 24 Jul 2020 16:24:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:24:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:24:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:24:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 19:00:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Jul 2020 19:00:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 19:00:19 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 19:00:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 19:00:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 19:00:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 19:00:58 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Jul 2020 19:01:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 19:01:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 11 Aug 2020 19:58:39 GMT
ENV MARIADB_VERSION=1:10.5.5+maria~focal
# Tue, 11 Aug 2020 19:58:41 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 11 Aug 2020 19:59:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 11 Aug 2020 19:59:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Aug 2020 19:59:53 GMT
COPY file:7a2bd14d0848358d403d6a9913bd5da8743de51ba46b60bf676d773828a634a0 in /usr/local/bin/ 
# Tue, 11 Aug 2020 19:59:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Aug 2020 19:59:55 GMT
EXPOSE 3306
# Tue, 11 Aug 2020 19:59:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3583fd5e2faf2976fb6333a3a15414f2708dc284c018a672e37112326bc7b7a1`  
		Last Modified: Mon, 20 Jul 2020 15:50:10 GMT  
		Size: 27.2 MB (27159444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2d9e0aed378588f59f8f4276e70ea379b773d7d6507046cd7a044601499785`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 32.3 KB (32333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a6dca9e536449681a937b8f49022cb56b230e352da8aed9b616fadb14dc30`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d9e98650a6106452fc9e640abe8929399fa4f7a0d3ef58a593e8d68cdf3a6`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe7adb1fa2ddb69c79f848dc8e063035d0470e286b22ba7655c53454d6ebff7`  
		Last Modified: Fri, 24 Jul 2020 19:08:00 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd004b5e1b54f4369864ebbfc0483cdc0f1968abc4fe137808aba5c6f991dd`  
		Last Modified: Fri, 24 Jul 2020 19:08:01 GMT  
		Size: 5.5 MB (5454207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4510b219e19a34d3e00b555c60de91322477c0ce69e09eecdf9e37c955cbee`  
		Last Modified: Fri, 24 Jul 2020 19:08:00 GMT  
		Size: 1.3 MB (1259467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcc4787d0abecd0bac521398d20a0951fa562de5cf186d6eeacc2247e5dec90`  
		Last Modified: Fri, 24 Jul 2020 19:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a727215d576269ce1cc4c41e2f8e45fdb29ee95b517d266f42eec3a5e6086860`  
		Last Modified: Fri, 24 Jul 2020 19:07:58 GMT  
		Size: 1.3 MB (1263910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d499a498ecfb277a39415faa8b1794c0794b37745444230292b6db2b677525f`  
		Last Modified: Fri, 24 Jul 2020 19:07:57 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de546d51e72ebcf6dae16bd8d26f7ae6abb8cb0dc843bc0dd93c5eb79c1d0101`  
		Last Modified: Tue, 11 Aug 2020 20:06:37 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700b74c14961a44e7fa2bc890993ad33b84ea241dc015e35bb3e303a74a400b8`  
		Last Modified: Tue, 11 Aug 2020 20:07:06 GMT  
		Size: 88.0 MB (88046117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96866cb8cd5412db0e4d36dff066c1d944ae2f0937509c870bce64fff8a5c02d`  
		Last Modified: Tue, 11 Aug 2020 20:06:37 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a7803e8939d15e80ac32eaea4b072884b3d335133fb679c7cd103fad75dafa9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135634352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95db865e1c45ea6602ba297ecfd8c914dd70591bbe475c18b561eb6bf6f0c115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Jul 2020 14:35:30 GMT
ADD file:fec1d8aac4ab3a3c2326e15808c04b0df4c06c2c4e66d3f34e3e31d3408fd793 in / 
# Fri, 24 Jul 2020 14:35:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:36:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:36:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:36:43 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:43:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 24 Jul 2020 16:46:48 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:46:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:47:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:47:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:48:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:48:31 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 24 Jul 2020 16:48:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:48:48 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 11 Aug 2020 21:13:15 GMT
ENV MARIADB_VERSION=1:10.5.5+maria~focal
# Tue, 11 Aug 2020 21:13:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 11 Aug 2020 21:18:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 11 Aug 2020 21:18:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Aug 2020 21:18:51 GMT
COPY file:7a2bd14d0848358d403d6a9913bd5da8743de51ba46b60bf676d773828a634a0 in /usr/local/bin/ 
# Tue, 11 Aug 2020 21:18:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Aug 2020 21:19:00 GMT
EXPOSE 3306
# Tue, 11 Aug 2020 21:19:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4739cd2f4f486596c583c79f6033f1a9dee019389d512603609494678c8ccd53`  
		Last Modified: Mon, 20 Jul 2020 15:51:10 GMT  
		Size: 33.3 MB (33279182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f57f5c67707a22a55ae858c6c54f236321b919889f34c321e1a3cc35b9a7988`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 32.2 KB (32166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169b0395dde9514c1a521632a61afda1494fe836f816badcab196bd067b4891c`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b459fe5e4dff59e4cc2b4b5207df42a369d6f0ac774f26c55184b3ccd491996`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bef61adb8f5adc075a1b8311c720b2188c8ab7227945e6e045104baf1a73d8`  
		Last Modified: Fri, 24 Jul 2020 17:16:52 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a1493e176fbe3f6d7f1fd0966e7f2279cdc3fa28332b6ae8dbc268809061a1`  
		Last Modified: Fri, 24 Jul 2020 17:16:54 GMT  
		Size: 6.7 MB (6667795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a85d2e1dc8b5cc93f651e75fc8c80d9c173996d74d8e92368b24288e4d60e9`  
		Last Modified: Fri, 24 Jul 2020 17:16:50 GMT  
		Size: 1.2 MB (1242901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef787355c45f11ab04446b3b08f253fa28239544319718af869047a7ac06cb43`  
		Last Modified: Fri, 24 Jul 2020 17:16:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c60e07e6eccc70f07c76340890aa85eab982223f556555e9df6a3865a5ef1b`  
		Last Modified: Fri, 24 Jul 2020 17:16:47 GMT  
		Size: 1.3 MB (1276142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073647b88667cfab796996c2a9b68007b4ef113a64d6c68c1577c8fe729ac406`  
		Last Modified: Fri, 24 Jul 2020 17:16:46 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcbe7bb601dbac7c096ab479cae1cd9ad27c4948b1022719848cd8eb762c1bc`  
		Last Modified: Tue, 11 Aug 2020 21:38:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2e0b3f97158c2e8a00c06bbcb0544f611b95351ad3bd6df965ce24a9b69e76`  
		Last Modified: Tue, 11 Aug 2020 21:39:07 GMT  
		Size: 93.1 MB (93125328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9439c437b60b1f2923382278d74a80cf5111154dd962614c080402c30c2e32`  
		Last Modified: Tue, 11 Aug 2020 21:38:46 GMT  
		Size: 5.1 KB (5061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
