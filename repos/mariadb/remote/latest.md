## `mariadb:latest`

```console
$ docker pull mariadb@sha256:a62bf6dd62bf71f1fa66887b1d3e0a9d6a7583e6a5ff08df4e53f4451d2c1571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:fd8fca1db97afb815fb3d61b0059101b3174938cc6e44aa9ced0cd65788004fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113176470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93d99aa9076c3582e36fd458be51d2d389cf421b711f03b8767f156be4d2cfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:59:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 31 Oct 2019 22:59:27 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:28 GMT
ENV GOSU_VERSION=1.10
# Thu, 31 Oct 2019 22:59:40 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 31 Oct 2019 22:59:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 22:59:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:48 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 31 Oct 2019 22:59:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 22:59:49 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 12 Dec 2019 23:29:13 GMT
ENV MARIADB_VERSION=1:10.4.11+maria~bionic
# Thu, 12 Dec 2019 23:29:14 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 12 Dec 2019 23:29:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 12 Dec 2019 23:29:47 GMT
VOLUME [/var/lib/mysql]
# Thu, 12 Dec 2019 23:29:47 GMT
COPY file:e4a8478ac83a333651c27c5a51a24850e0d3c4dc7c17fef2e5674014e3485df8 in /usr/local/bin/ 
# Thu, 12 Dec 2019 23:29:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 12 Dec 2019 23:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2019 23:29:48 GMT
EXPOSE 3306
# Thu, 12 Dec 2019 23:29:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215d801d026333c9167f6adfe47166d4f0c4c0d2b42bba8e8e0a04a87474427f`  
		Last Modified: Thu, 31 Oct 2019 23:03:34 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59feacde9e0873f2f58c384307f211f814237a4e0ad7a2e1b024a354cf6edac3`  
		Last Modified: Thu, 31 Oct 2019 23:03:34 GMT  
		Size: 4.8 MB (4806039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741aa98d779c1bb98e2f8b7fff2d11ef6b25fe63f81d3558d78545f16e6fbbe3`  
		Last Modified: Thu, 31 Oct 2019 23:03:33 GMT  
		Size: 866.8 KB (866821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f771d07df1b6b9589bbb07de679a21b2283402a22cd26f549d7302be7e5f61`  
		Last Modified: Thu, 31 Oct 2019 23:03:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38be307a8063d66ba338584a8c466192d55c3c30eadd9726990b47e35168a2be`  
		Last Modified: Thu, 31 Oct 2019 23:03:33 GMT  
		Size: 874.4 KB (874418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef9df553f6df85d27ed451a3131bfad6ec9fc17194d218541ea03b1f98001c1`  
		Last Modified: Thu, 31 Oct 2019 23:03:31 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541883163c4aafd7b61b6a8cfce7120a8738fa6cf1509597e168fa5e8bf2c404`  
		Last Modified: Thu, 12 Dec 2019 23:31:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f6a2b3e2d1e32b014948d2ed6a0db2c74c690eed381297d4bbfaa87ff1cc6f`  
		Last Modified: Thu, 12 Dec 2019 23:31:39 GMT  
		Size: 79.9 MB (79891806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5fe4ad1385da377cb99a2bee9b14338bfe4b6923118926aa0042b8ef26dc2e`  
		Last Modified: Thu, 12 Dec 2019 23:31:14 GMT  
		Size: 4.7 KB (4709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df452bf3dcd6532f8250d8461841b825f386550e6bb5886e7e25ee95e226d1`  
		Last Modified: Thu, 12 Dec 2019 23:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b8a1f497605d78bb629b8a9153a2e3aeba7a7459a273a0ea02263798f52c329d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108414291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855413f5e48e064d29a7cfef2f27b5d5da2b4b8881e1e982c731be3acd625e70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:04:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 31 Oct 2019 23:04:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:04:56 GMT
ENV GOSU_VERSION=1.10
# Thu, 31 Oct 2019 23:05:13 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 31 Oct 2019 23:05:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:05:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:05:27 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 31 Oct 2019 23:05:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:05:30 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 12 Dec 2019 23:42:54 GMT
ENV MARIADB_VERSION=1:10.4.11+maria~bionic
# Thu, 12 Dec 2019 23:42:55 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 12 Dec 2019 23:43:35 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 12 Dec 2019 23:43:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 12 Dec 2019 23:43:37 GMT
COPY file:e4a8478ac83a333651c27c5a51a24850e0d3c4dc7c17fef2e5674014e3485df8 in /usr/local/bin/ 
# Thu, 12 Dec 2019 23:43:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 12 Dec 2019 23:43:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2019 23:43:40 GMT
EXPOSE 3306
# Thu, 12 Dec 2019 23:43:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcef89e3002685a2073816604313e93a8fdb3763a9cb74851089c6723855251`  
		Last Modified: Thu, 31 Oct 2019 23:09:50 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06115e3e56a019a03414167d44e914a6434feb1ddbbcd410b0fb9f22ff2b483d`  
		Last Modified: Thu, 31 Oct 2019 23:09:50 GMT  
		Size: 4.4 MB (4391853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5712e955a6d4450278d3f5086f5903029401b07e9f39020b6330b49fd40790d4`  
		Last Modified: Thu, 31 Oct 2019 23:09:49 GMT  
		Size: 833.7 KB (833663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd2dc9f5e8f708cdb5edcf8a4a4a318da0d8e364995acf9d62704ae08fe4855`  
		Last Modified: Thu, 31 Oct 2019 23:09:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ef8ef990de1d87703fbcf5fbe50f3d772eac7778bf5cc7d6b0c20454f4473c`  
		Last Modified: Thu, 31 Oct 2019 23:09:49 GMT  
		Size: 873.6 KB (873583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae55899885f17f0ea18611dcfb3b08c10e5b74b18ecb06ddb6b13c4f92866585`  
		Last Modified: Thu, 31 Oct 2019 23:09:47 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b950ea4bb7d908b86ba5b35154a10ca7f0ab475fd28db308702fd736e94e314`  
		Last Modified: Thu, 12 Dec 2019 23:46:16 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2f575de51fdc5411e8fc8d7c33da8bd76d311d56295b84cc29580bfabd0267`  
		Last Modified: Thu, 12 Dec 2019 23:46:39 GMT  
		Size: 78.5 MB (78548341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b741353c7c5235b7dc490904ad3219d1ebd63cbf6d93c68cbb42cd550c94d93c`  
		Last Modified: Thu, 12 Dec 2019 23:46:16 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66809a00bff0f89d4582d7024907e0aaa41820aec076e80ae19687c138e8a5b7`  
		Last Modified: Thu, 12 Dec 2019 23:46:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:caf1cdbd1161ee8f22338fa71b58841b2035d021f430d9e0eafc2495d3df67a3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120875286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93011e9a559526e5e4474316d36669252216b6d239f72b38de4f50ac36aad453`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:59:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 31 Oct 2019 23:00:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:00:38 GMT
ENV GOSU_VERSION=1.10
# Thu, 31 Oct 2019 23:01:16 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 31 Oct 2019 23:01:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:01:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:01:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 31 Oct 2019 23:01:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:01:45 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 13 Dec 2019 00:16:40 GMT
ENV MARIADB_VERSION=1:10.4.11+maria~bionic
# Fri, 13 Dec 2019 00:16:47 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 13 Dec 2019 00:18:48 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 13 Dec 2019 00:18:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Dec 2019 00:18:56 GMT
COPY file:e4a8478ac83a333651c27c5a51a24850e0d3c4dc7c17fef2e5674014e3485df8 in /usr/local/bin/ 
# Fri, 13 Dec 2019 00:19:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Dec 2019 00:19:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2019 00:19:12 GMT
EXPOSE 3306
# Fri, 13 Dec 2019 00:19:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d89284e72162855e101ace8b4f617c76a8c416a3dbb38363ef11bc3134cc2d`  
		Last Modified: Thu, 31 Oct 2019 23:07:48 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aad457c20bb984ef2808695aa1f5e1ee80fbe602da3076fdbacf6c51660555`  
		Last Modified: Thu, 31 Oct 2019 23:07:49 GMT  
		Size: 5.6 MB (5627595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30586365750a352c3873e548412a67fd58964287f0f4d1f2ab030a14f4731bf`  
		Last Modified: Thu, 31 Oct 2019 23:07:46 GMT  
		Size: 835.7 KB (835720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ccd6dc0526044343428be47cba303fc666293f7028e76e76c0ad69c5cb9e7a`  
		Last Modified: Thu, 31 Oct 2019 23:07:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959319a59aec61caaf5605d4cfddea271d0a3d93093d32afad8169e59bb2c03c`  
		Last Modified: Thu, 31 Oct 2019 23:07:46 GMT  
		Size: 875.2 KB (875164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5482a7c772ac9aba4b1c3a512d67ec73535e43a63ecc6abf4d7ebe67a6d35977`  
		Last Modified: Thu, 31 Oct 2019 23:07:42 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825cd2f830c6db7f707281a2b8c29e5764c32c1b0cfc031ae8da7fb81cdc2ca4`  
		Last Modified: Fri, 13 Dec 2019 00:24:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52270a53b85b1d63430340b4a58b165fd8fcd4c2e52ca2e5f7df9e3f9df7f2a3`  
		Last Modified: Fri, 13 Dec 2019 00:25:01 GMT  
		Size: 83.1 MB (83088953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66dd5b290d7e6476146bbc4420e9c9063509f49ad1b180d8d8023e281f62597`  
		Last Modified: Fri, 13 Dec 2019 00:24:42 GMT  
		Size: 4.7 KB (4710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f95cfd97752f9dc0d45e17f0b420f4edf7a5f93afc9fc8ce8e69ea2330720`  
		Last Modified: Fri, 13 Dec 2019 00:24:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
