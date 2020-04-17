## `mariadb:beta`

```console
$ docker pull mariadb@sha256:2ff7c83f7f3b7a565d3920fecd7287dc47a1af1a05fbe234fcac1bb22bd2dd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta` - linux; amd64

```console
$ docker pull mariadb@sha256:431dc6648289340ee1f51b1e943474f0215c592f33355ec36b03b405b382df5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114233597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce2a7ed8efd4da2668489b15de307e3c1b743e250054258af6f91fe7bc13566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:07:57 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 20 Mar 2020 20:08:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:08:05 GMT
ENV GOSU_VERSION=1.10
# Fri, 20 Mar 2020 20:08:14 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 20 Mar 2020 20:08:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 20 Mar 2020 20:08:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:08:22 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 20 Mar 2020 20:08:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 20 Mar 2020 20:08:23 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 31 Mar 2020 00:30:20 GMT
ENV MARIADB_VERSION=1:10.5.2+maria~bionic
# Tue, 31 Mar 2020 00:30:21 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 31 Mar 2020 00:30:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 00:30:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 00:30:54 GMT
COPY file:11e6bb0ed0a4518785c4affa0b36a550b4858cf10b7b87cc4d99296eaeabe9f2 in /usr/local/bin/ 
# Tue, 31 Mar 2020 00:30:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 00:30:54 GMT
EXPOSE 3306
# Tue, 31 Mar 2020 00:30:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e3c043ec689651a0d36c0ec99c38a8b2fabd1126bf07ca3add42ec3d6d0ac7`  
		Last Modified: Fri, 20 Mar 2020 20:11:51 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141e45c6af4bfa80295fe6fe19f3a76fd69f260eafeca26bc9b625b89fdfc3ef`  
		Last Modified: Fri, 20 Mar 2020 20:11:51 GMT  
		Size: 4.8 MB (4808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26245908a82e62155c2d10d7b7152341c5172f259020f17dd5ca186c5736c30`  
		Last Modified: Fri, 20 Mar 2020 20:11:51 GMT  
		Size: 867.7 KB (867691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ccaf895c8a33b8c6e3bc1d8065e4ef31442809d70d3eaefa1fc2899f91540e`  
		Last Modified: Fri, 20 Mar 2020 20:11:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d665f60c94a9bce6313853ec27d3e977394c13196fc732ee44aca2de166f26e`  
		Last Modified: Fri, 20 Mar 2020 20:11:50 GMT  
		Size: 930.0 KB (929979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bcd9961bee1d541ab21b169b9d8e826a8d7abccfca865c7ea9727bf6bbfd87`  
		Last Modified: Fri, 20 Mar 2020 20:11:49 GMT  
		Size: 5.2 KB (5169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fc6bfc4f267a6477169329e5c78818791c7eccc258256b5093eaed850411a3`  
		Last Modified: Tue, 31 Mar 2020 00:31:21 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ea2580e7ab6bc1a2c0421933910645abccd720ac1248352c1c317727a7313`  
		Last Modified: Tue, 31 Mar 2020 00:31:53 GMT  
		Size: 80.9 MB (80888489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5b9f72433f5f5058db43b6f4490dc6b27832228a63f9d2d4481cf963aba461`  
		Last Modified: Tue, 31 Mar 2020 00:31:21 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9b95e01119f094ce4b0ecef02d6a06ffa85ae7d3a460ef7cfd1238648e7d1fd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109812109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72a39df7c52ad770213ca7081d373a2beb269e946217e1d6262ae1b4e9edbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2020 18:43:33 GMT
ADD file:e4214b65d372c2f971e6544f69c465e8b1ba82290276558036047179a02ba9e3 in / 
# Fri, 20 Mar 2020 18:43:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:43:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:43:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:43:39 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:26:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 20 Mar 2020 19:26:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:56:15 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 10:56:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 10:56:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 10:57:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:57:09 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 17 Apr 2020 10:57:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 10:57:13 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 17 Apr 2020 10:57:14 GMT
ENV MARIADB_VERSION=1:10.5.2+maria~bionic
# Fri, 17 Apr 2020 10:57:17 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 17 Apr 2020 10:58:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 17 Apr 2020 10:58:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 17 Apr 2020 10:58:21 GMT
COPY file:11e6bb0ed0a4518785c4affa0b36a550b4858cf10b7b87cc4d99296eaeabe9f2 in /usr/local/bin/ 
# Fri, 17 Apr 2020 10:58:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:58:22 GMT
EXPOSE 3306
# Fri, 17 Apr 2020 10:58:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b2f61026a351316126bfad6f6cac3971b3b3e928b126ac53026bb4263459d2ff`  
		Last Modified: Mon, 16 Mar 2020 15:39:01 GMT  
		Size: 23.7 MB (23720219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538fb30c42c023ad64c0e31ce3cb02e3c4150f9ac944a46d3386b8212b80043`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 35.2 KB (35206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b05810781a3c493e08dc6e2c9b9553244f8f86248f7d709a50becbac344234`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a33352d6b41ad6ca5fac27544fb3c8c7cb69e67dc30bf9584b49cd3b3938`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee461e1660472551faa4abda985ed0a33b8d07fc0bc30aa296e7afd3ccb7285a`  
		Last Modified: Fri, 20 Mar 2020 19:32:42 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea90ab252c57ae08c8e7729133de6428422c2f0635288e90061f8150ffdcdcc8`  
		Last Modified: Fri, 20 Mar 2020 19:32:43 GMT  
		Size: 4.4 MB (4392992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af2d6b10013b7a151e2a71df993748b441485369c48690cf412507cd48fdd3`  
		Last Modified: Fri, 17 Apr 2020 11:04:20 GMT  
		Size: 1.3 MB (1262815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0399fa3e97b58c12e1641c7bf2590f686a5f1cb72f1809901544120fec64e0a`  
		Last Modified: Fri, 17 Apr 2020 11:04:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cd73f97047b70ee6fa7b6f95aa2c45cb84644ddb1d2f6e5ca192205bbfddde`  
		Last Modified: Fri, 17 Apr 2020 11:04:17 GMT  
		Size: 920.7 KB (920718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a22210d2ced978bc985fb12770be08a0fbebbbc5f0ab215dfa7d43fbb28c8f`  
		Last Modified: Fri, 17 Apr 2020 11:04:17 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706a9df3d918103eed1579d1519a74af032a54378f739fa3dd840be5be5246e`  
		Last Modified: Fri, 17 Apr 2020 11:04:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea604a8c60c146df4f9133b7c8e86fed48c7bd606f4c99d46df1d39ae55db5`  
		Last Modified: Fri, 17 Apr 2020 11:04:39 GMT  
		Size: 79.5 MB (79466820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e057041d8bcc6c5033df19caf275d03490b648b8394b49f451e67f520fda18d4`  
		Last Modified: Fri, 17 Apr 2020 11:04:17 GMT  
		Size: 4.8 KB (4765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bddd1f75c96cfd01d287966cc6111fdcc9415d206fce61844e4af1f48d5ddfa5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121880386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28d34a74323db15e744d1d7eb8f287468ba8b72aa07f6b0b2db4dddad0f0398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2020 19:22:18 GMT
ADD file:226ecdf321a0fde3bea0d6e88db018b3d077f676a1f1e06942217ebb26a02301 in / 
# Fri, 20 Mar 2020 19:22:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:22:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:22:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:22:44 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 21:02:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 20 Mar 2020 21:03:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 21:03:44 GMT
ENV GOSU_VERSION=1.10
# Fri, 20 Mar 2020 21:04:34 GMT
RUN set -ex; 		fetchDeps=' 		ca-certificates 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 20 Mar 2020 21:04:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 20 Mar 2020 21:05:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 21:05:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 20 Mar 2020 21:05:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 20 Mar 2020 21:05:16 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 31 Mar 2020 00:42:03 GMT
ENV MARIADB_VERSION=1:10.5.2+maria~bionic
# Tue, 31 Mar 2020 00:42:11 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 31 Mar 2020 00:44:26 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 00:44:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 00:44:36 GMT
COPY file:11e6bb0ed0a4518785c4affa0b36a550b4858cf10b7b87cc4d99296eaeabe9f2 in /usr/local/bin/ 
# Tue, 31 Mar 2020 00:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 00:44:43 GMT
EXPOSE 3306
# Tue, 31 Mar 2020 00:44:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:044eae4257f9584af1a24a5cdb9754c96aea36080e68260ddbabab04827bac00`  
		Last Modified: Mon, 16 Mar 2020 15:38:59 GMT  
		Size: 30.4 MB (30399915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf63a142f3acf0fc36d344bc173f2e1990e692aff0c1237ed6dc96cf38cfb2e`  
		Last Modified: Fri, 20 Mar 2020 19:25:02 GMT  
		Size: 35.2 KB (35212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d9f5f16809d964026266c73b1c06d3cc0dc517437a91d8639758b80958679`  
		Last Modified: Fri, 20 Mar 2020 19:25:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34444f41441c2f598f5dda94ec1b47ee527ce6e5025d70e5eea41a400d16b1`  
		Last Modified: Fri, 20 Mar 2020 19:25:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db5fac46cdbd09215d127fce60ab919bd0eef894020af8b2c4998bb29c952c9`  
		Last Modified: Fri, 20 Mar 2020 21:23:17 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb78b03dbc6a15f9f463408efdcb18de025cb202153aea8a26bed844cdf8d81`  
		Last Modified: Fri, 20 Mar 2020 21:23:18 GMT  
		Size: 5.6 MB (5628622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8968be23f6c8c2109905c8450f83693954eda1cca3a407bf05540423bbd137`  
		Last Modified: Fri, 20 Mar 2020 21:23:16 GMT  
		Size: 835.8 KB (835806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5b2693e120a91c8f20e9606bd43812ff53870f1bca10a5ff2dbaf2859eac95`  
		Last Modified: Fri, 20 Mar 2020 21:23:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb535078ba01d3856073095f2c6aab5e1dac7ef049a328ed3e377609ea2448`  
		Last Modified: Fri, 20 Mar 2020 21:23:14 GMT  
		Size: 931.5 KB (931508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af7cb734719529a2598539f44d2d9788cfb85b3c3a98862c81b50a6028ecade`  
		Last Modified: Fri, 20 Mar 2020 21:23:13 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8dac0471f1f43edc679b3f3f8158c52e78d29021d25d30ed56d23a59e2a676`  
		Last Modified: Tue, 31 Mar 2020 00:45:28 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817678fd4b822911d332eb865141489e2a0c86cf2896c40c12ffe15a0d5dd14d`  
		Last Modified: Tue, 31 Mar 2020 00:45:48 GMT  
		Size: 84.0 MB (84035993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e685f89a7587a47fd9b06ffb729ec41bce7b4c9721b6774ff536a372713d8598`  
		Last Modified: Tue, 31 Mar 2020 00:45:28 GMT  
		Size: 4.8 KB (4765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
