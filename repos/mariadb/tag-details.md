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
-	[`mariadb:10.5.4`](#mariadb1054)
-	[`mariadb:10.5.4-focal`](#mariadb1054-focal)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1`

```console
$ docker pull mariadb@sha256:8dda3c42d4130e9315eec7eff96714bb47dfc541740f28b7d1ee73e6de636c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1` - linux; amd64

```console
$ docker pull mariadb@sha256:47969ceafe0183bc8f4555c232e1666ec2634fe8f865cb1f6350facb6a91a50a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113195933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041a88df58c7fe7a7163fab9ae86bcfd3eee6983a363d35306a6528fec684b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:23:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:24:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:04 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:05 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:06 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6f108ab29756672d51795848e2d285bfa6b45ea44d73a6944eec029e72c7aa`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50590ce9d712ae5907362d5f4817aa6c3ba57834c45c06f397742736580c51b`  
		Last Modified: Tue, 07 Jul 2020 00:26:05 GMT  
		Size: 79.4 MB (79387577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca211364ad9fe90fc811c6d108bfcf9c320ea28e7db8c27edc307346ab80df98`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab87514a02e00c93d5e71c0a34060fc5376aae706d3c758b9049860d3436a606`  
		Last Modified: Tue, 07 Jul 2020 00:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:45de747f692e40f4975ac9c9c4e2a777c7a0542cabed0ee7403c1d8027ddab31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105803215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53482825afb13c6db322cd32f67b34ef1f60eb7cb166d39b1344df8a1b1eaa6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:49:20 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:49:21 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:49:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:50:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:50:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:50:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:50:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:50:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:50:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba7857d9511a39b5cc294bba768d957487ae21e3960db01ba77892307ed9d7`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c25e851cf532ec38a4373a4ddb6fcef8491d0d03e31eddefd1534de0059711`  
		Last Modified: Tue, 07 Jul 2020 00:53:42 GMT  
		Size: 75.5 MB (75458050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32067bc4007446a3754682b113c7f96284b19360e68ad0459f894d636040139`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54203ec464ded38af1420076c7564f7ee0fc05f974d4f22f5d9a4ae4b86d2d3`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d18833b20dd4db22a78625a33d0733b45e78eff86dfb63e9d6da7c2b34540504
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118198044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8992028116652a047f6f6b7349952b51470f713e93d0fadf097ef349368264b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:32:09 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:32:12 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:32:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:35:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:35:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:35:41 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:35:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:36:02 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:36:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cb39ae37f688d990674993d559082d7d204ebf6ae1a2a7bbc7fad428f7e18`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc189648336f6c3994281560163d5b44f32c21df96952aa9fb0c4f9a65f719`  
		Last Modified: Tue, 07 Jul 2020 00:40:12 GMT  
		Size: 79.9 MB (79938700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd2669a7749565a3c6dcebd29fda023804ff96f3f5d1709a542e71e6a56f3bd`  
		Last Modified: Tue, 07 Jul 2020 00:39:54 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef2f1effff2f345bd0a00b067a650393a1b63b67dcdf55e079540b12ab8a74`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45`

```console
$ docker pull mariadb@sha256:8dda3c42d4130e9315eec7eff96714bb47dfc541740f28b7d1ee73e6de636c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45` - linux; amd64

```console
$ docker pull mariadb@sha256:47969ceafe0183bc8f4555c232e1666ec2634fe8f865cb1f6350facb6a91a50a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113195933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041a88df58c7fe7a7163fab9ae86bcfd3eee6983a363d35306a6528fec684b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:23:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:24:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:04 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:05 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:06 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6f108ab29756672d51795848e2d285bfa6b45ea44d73a6944eec029e72c7aa`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50590ce9d712ae5907362d5f4817aa6c3ba57834c45c06f397742736580c51b`  
		Last Modified: Tue, 07 Jul 2020 00:26:05 GMT  
		Size: 79.4 MB (79387577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca211364ad9fe90fc811c6d108bfcf9c320ea28e7db8c27edc307346ab80df98`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab87514a02e00c93d5e71c0a34060fc5376aae706d3c758b9049860d3436a606`  
		Last Modified: Tue, 07 Jul 2020 00:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:45de747f692e40f4975ac9c9c4e2a777c7a0542cabed0ee7403c1d8027ddab31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105803215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53482825afb13c6db322cd32f67b34ef1f60eb7cb166d39b1344df8a1b1eaa6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:49:20 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:49:21 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:49:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:50:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:50:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:50:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:50:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:50:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:50:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba7857d9511a39b5cc294bba768d957487ae21e3960db01ba77892307ed9d7`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c25e851cf532ec38a4373a4ddb6fcef8491d0d03e31eddefd1534de0059711`  
		Last Modified: Tue, 07 Jul 2020 00:53:42 GMT  
		Size: 75.5 MB (75458050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32067bc4007446a3754682b113c7f96284b19360e68ad0459f894d636040139`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54203ec464ded38af1420076c7564f7ee0fc05f974d4f22f5d9a4ae4b86d2d3`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d18833b20dd4db22a78625a33d0733b45e78eff86dfb63e9d6da7c2b34540504
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118198044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8992028116652a047f6f6b7349952b51470f713e93d0fadf097ef349368264b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:32:09 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:32:12 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:32:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:35:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:35:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:35:41 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:35:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:36:02 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:36:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cb39ae37f688d990674993d559082d7d204ebf6ae1a2a7bbc7fad428f7e18`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc189648336f6c3994281560163d5b44f32c21df96952aa9fb0c4f9a65f719`  
		Last Modified: Tue, 07 Jul 2020 00:40:12 GMT  
		Size: 79.9 MB (79938700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd2669a7749565a3c6dcebd29fda023804ff96f3f5d1709a542e71e6a56f3bd`  
		Last Modified: Tue, 07 Jul 2020 00:39:54 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef2f1effff2f345bd0a00b067a650393a1b63b67dcdf55e079540b12ab8a74`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.45-bionic`

```console
$ docker pull mariadb@sha256:8dda3c42d4130e9315eec7eff96714bb47dfc541740f28b7d1ee73e6de636c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.45-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:47969ceafe0183bc8f4555c232e1666ec2634fe8f865cb1f6350facb6a91a50a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113195933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041a88df58c7fe7a7163fab9ae86bcfd3eee6983a363d35306a6528fec684b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:23:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:24:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:04 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:05 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:06 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6f108ab29756672d51795848e2d285bfa6b45ea44d73a6944eec029e72c7aa`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50590ce9d712ae5907362d5f4817aa6c3ba57834c45c06f397742736580c51b`  
		Last Modified: Tue, 07 Jul 2020 00:26:05 GMT  
		Size: 79.4 MB (79387577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca211364ad9fe90fc811c6d108bfcf9c320ea28e7db8c27edc307346ab80df98`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab87514a02e00c93d5e71c0a34060fc5376aae706d3c758b9049860d3436a606`  
		Last Modified: Tue, 07 Jul 2020 00:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:45de747f692e40f4975ac9c9c4e2a777c7a0542cabed0ee7403c1d8027ddab31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105803215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53482825afb13c6db322cd32f67b34ef1f60eb7cb166d39b1344df8a1b1eaa6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:49:20 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:49:21 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:49:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:50:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:50:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:50:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:50:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:50:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:50:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba7857d9511a39b5cc294bba768d957487ae21e3960db01ba77892307ed9d7`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c25e851cf532ec38a4373a4ddb6fcef8491d0d03e31eddefd1534de0059711`  
		Last Modified: Tue, 07 Jul 2020 00:53:42 GMT  
		Size: 75.5 MB (75458050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32067bc4007446a3754682b113c7f96284b19360e68ad0459f894d636040139`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54203ec464ded38af1420076c7564f7ee0fc05f974d4f22f5d9a4ae4b86d2d3`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.45-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d18833b20dd4db22a78625a33d0733b45e78eff86dfb63e9d6da7c2b34540504
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118198044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8992028116652a047f6f6b7349952b51470f713e93d0fadf097ef349368264b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:32:09 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:32:12 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:32:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:35:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:35:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:35:41 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:35:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:36:02 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:36:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cb39ae37f688d990674993d559082d7d204ebf6ae1a2a7bbc7fad428f7e18`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc189648336f6c3994281560163d5b44f32c21df96952aa9fb0c4f9a65f719`  
		Last Modified: Tue, 07 Jul 2020 00:40:12 GMT  
		Size: 79.9 MB (79938700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd2669a7749565a3c6dcebd29fda023804ff96f3f5d1709a542e71e6a56f3bd`  
		Last Modified: Tue, 07 Jul 2020 00:39:54 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef2f1effff2f345bd0a00b067a650393a1b63b67dcdf55e079540b12ab8a74`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1-bionic`

```console
$ docker pull mariadb@sha256:8dda3c42d4130e9315eec7eff96714bb47dfc541740f28b7d1ee73e6de636c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:47969ceafe0183bc8f4555c232e1666ec2634fe8f865cb1f6350facb6a91a50a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113195933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041a88df58c7fe7a7163fab9ae86bcfd3eee6983a363d35306a6528fec684b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:23:17 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:23:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:24:04 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:04 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:05 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:06 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6f108ab29756672d51795848e2d285bfa6b45ea44d73a6944eec029e72c7aa`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50590ce9d712ae5907362d5f4817aa6c3ba57834c45c06f397742736580c51b`  
		Last Modified: Tue, 07 Jul 2020 00:26:05 GMT  
		Size: 79.4 MB (79387577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca211364ad9fe90fc811c6d108bfcf9c320ea28e7db8c27edc307346ab80df98`  
		Last Modified: Tue, 07 Jul 2020 00:25:50 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab87514a02e00c93d5e71c0a34060fc5376aae706d3c758b9049860d3436a606`  
		Last Modified: Tue, 07 Jul 2020 00:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:45de747f692e40f4975ac9c9c4e2a777c7a0542cabed0ee7403c1d8027ddab31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105803215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53482825afb13c6db322cd32f67b34ef1f60eb7cb166d39b1344df8a1b1eaa6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:49:20 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:49:21 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:49:22 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:50:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:50:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:50:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:50:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:50:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:50:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba7857d9511a39b5cc294bba768d957487ae21e3960db01ba77892307ed9d7`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c25e851cf532ec38a4373a4ddb6fcef8491d0d03e31eddefd1534de0059711`  
		Last Modified: Tue, 07 Jul 2020 00:53:42 GMT  
		Size: 75.5 MB (75458050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32067bc4007446a3754682b113c7f96284b19360e68ad0459f894d636040139`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54203ec464ded38af1420076c7564f7ee0fc05f974d4f22f5d9a4ae4b86d2d3`  
		Last Modified: Tue, 07 Jul 2020 00:53:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d18833b20dd4db22a78625a33d0733b45e78eff86dfb63e9d6da7c2b34540504
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118198044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8992028116652a047f6f6b7349952b51470f713e93d0fadf097ef349368264b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:32:09 GMT
ENV MARIADB_MAJOR=10.1
# Tue, 07 Jul 2020 00:32:12 GMT
ENV MARIADB_VERSION=1:10.1.45+maria-1~bionic
# Tue, 07 Jul 2020 00:32:23 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:35:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:35:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:35:41 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:35:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:36:02 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:36:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cb39ae37f688d990674993d559082d7d204ebf6ae1a2a7bbc7fad428f7e18`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc189648336f6c3994281560163d5b44f32c21df96952aa9fb0c4f9a65f719`  
		Last Modified: Tue, 07 Jul 2020 00:40:12 GMT  
		Size: 79.9 MB (79938700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd2669a7749565a3c6dcebd29fda023804ff96f3f5d1709a542e71e6a56f3bd`  
		Last Modified: Tue, 07 Jul 2020 00:39:54 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef2f1effff2f345bd0a00b067a650393a1b63b67dcdf55e079540b12ab8a74`  
		Last Modified: Tue, 07 Jul 2020 00:39:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:7f9ef5c4dfd39efccbd80e6add152c672e6c63486874d83ce3f60c5a6ba33b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:bf1d6b81c8fe2f304241ad9507ad43cb95af1842ab55f0bfc8e0cb09202f1290
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109004709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e032f3ec5cfe68100563fb40dc1bad23fb4b10915e926b8b4e7dc69621aee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:22:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:03 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:23:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:23:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:23:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:23:05 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:23:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e647ff717838a99fa12f0d6eea2a7952ba37de10c4fcd23df83aeddac61fada`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6143f8fa886d375bf67bfc1ebb4d639a8539258372f5560e5aa7bdd12f282960`  
		Last Modified: Tue, 07 Jul 2020 00:25:45 GMT  
		Size: 75.2 MB (75196357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b866ec661a4ae2a4886cd514e3bb8eddd68a31c9cd2baab2ae5c916e0bcf8c3b`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c97cc2dea4fd3440b7fa98bbb890ab824fe2ec15891b864a0d1c9fd366fba7`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7efafa88f0a4c6586e57e6824cb5267da7ae6e1f8a95eb964adfc7f47eac7767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104078223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfdd6ddf350b7108c71ce0f5655da0c603feeb4cca8b99891e3e6b5124f067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:48:12 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:48:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:48:15 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:49:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:49:05 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:49:06 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:49:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:49:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:49:09 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:49:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491fe5a7106bd3fcdf9f4cd8716093c22f9da5b66d285bb95caca2cdec602c3a`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef303867e7f68b8e5c1cddc35fb8ef32c79f9c44d86813fddc3768ad46603f3`  
		Last Modified: Tue, 07 Jul 2020 00:53:10 GMT  
		Size: 73.7 MB (73733057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68561dfc9c7859add2f23eec8b2ce58c2bb6754057dfa0da9ebc4e57adc019b7`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e802a198f6cb745af2ad51bd56d39cd070039b83c12e19a526c8f91f1d2a8`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4b49f54779836d86370dde8a254ea883335d419d83ce9a31336fc6437637e34e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116244732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aee5709104dcc8bb906cc0066469e0159bc71a65a94a361abf5d76bd1659ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:28:11 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:28:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:28:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:31:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:31:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:31:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:31:40 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:31:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d98872d26d660f7078455773041269be26171d5608c90029e5a9ff9d42411`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0d0e6ce7eedbc6ab7a7e7a99a52f8a0993ecbf54b755aa4715d825d1390ad3`  
		Last Modified: Tue, 07 Jul 2020 00:39:24 GMT  
		Size: 78.0 MB (77985387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290725b4d016fff7987b6daa3b8718de754675576b668424d04d7150abb2736c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 4.9 KB (4858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f72ab411730ce6d7fb70a1fdaa64562269c69e72ef3a870464b352cbfa1cf`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32`

```console
$ docker pull mariadb@sha256:7f9ef5c4dfd39efccbd80e6add152c672e6c63486874d83ce3f60c5a6ba33b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32` - linux; amd64

```console
$ docker pull mariadb@sha256:bf1d6b81c8fe2f304241ad9507ad43cb95af1842ab55f0bfc8e0cb09202f1290
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109004709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e032f3ec5cfe68100563fb40dc1bad23fb4b10915e926b8b4e7dc69621aee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:22:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:03 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:23:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:23:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:23:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:23:05 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:23:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e647ff717838a99fa12f0d6eea2a7952ba37de10c4fcd23df83aeddac61fada`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6143f8fa886d375bf67bfc1ebb4d639a8539258372f5560e5aa7bdd12f282960`  
		Last Modified: Tue, 07 Jul 2020 00:25:45 GMT  
		Size: 75.2 MB (75196357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b866ec661a4ae2a4886cd514e3bb8eddd68a31c9cd2baab2ae5c916e0bcf8c3b`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c97cc2dea4fd3440b7fa98bbb890ab824fe2ec15891b864a0d1c9fd366fba7`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7efafa88f0a4c6586e57e6824cb5267da7ae6e1f8a95eb964adfc7f47eac7767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104078223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfdd6ddf350b7108c71ce0f5655da0c603feeb4cca8b99891e3e6b5124f067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:48:12 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:48:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:48:15 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:49:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:49:05 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:49:06 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:49:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:49:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:49:09 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:49:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491fe5a7106bd3fcdf9f4cd8716093c22f9da5b66d285bb95caca2cdec602c3a`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef303867e7f68b8e5c1cddc35fb8ef32c79f9c44d86813fddc3768ad46603f3`  
		Last Modified: Tue, 07 Jul 2020 00:53:10 GMT  
		Size: 73.7 MB (73733057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68561dfc9c7859add2f23eec8b2ce58c2bb6754057dfa0da9ebc4e57adc019b7`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e802a198f6cb745af2ad51bd56d39cd070039b83c12e19a526c8f91f1d2a8`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4b49f54779836d86370dde8a254ea883335d419d83ce9a31336fc6437637e34e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116244732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aee5709104dcc8bb906cc0066469e0159bc71a65a94a361abf5d76bd1659ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:28:11 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:28:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:28:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:31:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:31:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:31:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:31:40 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:31:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d98872d26d660f7078455773041269be26171d5608c90029e5a9ff9d42411`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0d0e6ce7eedbc6ab7a7e7a99a52f8a0993ecbf54b755aa4715d825d1390ad3`  
		Last Modified: Tue, 07 Jul 2020 00:39:24 GMT  
		Size: 78.0 MB (77985387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290725b4d016fff7987b6daa3b8718de754675576b668424d04d7150abb2736c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 4.9 KB (4858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f72ab411730ce6d7fb70a1fdaa64562269c69e72ef3a870464b352cbfa1cf`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.32-bionic`

```console
$ docker pull mariadb@sha256:7f9ef5c4dfd39efccbd80e6add152c672e6c63486874d83ce3f60c5a6ba33b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.32-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bf1d6b81c8fe2f304241ad9507ad43cb95af1842ab55f0bfc8e0cb09202f1290
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109004709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e032f3ec5cfe68100563fb40dc1bad23fb4b10915e926b8b4e7dc69621aee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:22:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:03 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:23:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:23:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:23:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:23:05 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:23:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e647ff717838a99fa12f0d6eea2a7952ba37de10c4fcd23df83aeddac61fada`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6143f8fa886d375bf67bfc1ebb4d639a8539258372f5560e5aa7bdd12f282960`  
		Last Modified: Tue, 07 Jul 2020 00:25:45 GMT  
		Size: 75.2 MB (75196357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b866ec661a4ae2a4886cd514e3bb8eddd68a31c9cd2baab2ae5c916e0bcf8c3b`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c97cc2dea4fd3440b7fa98bbb890ab824fe2ec15891b864a0d1c9fd366fba7`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7efafa88f0a4c6586e57e6824cb5267da7ae6e1f8a95eb964adfc7f47eac7767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104078223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfdd6ddf350b7108c71ce0f5655da0c603feeb4cca8b99891e3e6b5124f067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:48:12 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:48:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:48:15 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:49:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:49:05 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:49:06 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:49:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:49:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:49:09 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:49:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491fe5a7106bd3fcdf9f4cd8716093c22f9da5b66d285bb95caca2cdec602c3a`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef303867e7f68b8e5c1cddc35fb8ef32c79f9c44d86813fddc3768ad46603f3`  
		Last Modified: Tue, 07 Jul 2020 00:53:10 GMT  
		Size: 73.7 MB (73733057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68561dfc9c7859add2f23eec8b2ce58c2bb6754057dfa0da9ebc4e57adc019b7`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e802a198f6cb745af2ad51bd56d39cd070039b83c12e19a526c8f91f1d2a8`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.32-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4b49f54779836d86370dde8a254ea883335d419d83ce9a31336fc6437637e34e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116244732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aee5709104dcc8bb906cc0066469e0159bc71a65a94a361abf5d76bd1659ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:28:11 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:28:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:28:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:31:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:31:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:31:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:31:40 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:31:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d98872d26d660f7078455773041269be26171d5608c90029e5a9ff9d42411`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0d0e6ce7eedbc6ab7a7e7a99a52f8a0993ecbf54b755aa4715d825d1390ad3`  
		Last Modified: Tue, 07 Jul 2020 00:39:24 GMT  
		Size: 78.0 MB (77985387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290725b4d016fff7987b6daa3b8718de754675576b668424d04d7150abb2736c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 4.9 KB (4858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f72ab411730ce6d7fb70a1fdaa64562269c69e72ef3a870464b352cbfa1cf`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:7f9ef5c4dfd39efccbd80e6add152c672e6c63486874d83ce3f60c5a6ba33b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bf1d6b81c8fe2f304241ad9507ad43cb95af1842ab55f0bfc8e0cb09202f1290
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109004709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e032f3ec5cfe68100563fb40dc1bad23fb4b10915e926b8b4e7dc69621aee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:22:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:22:13 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:22:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:22:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:22:30 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:22:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:22:31 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:22:32 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:03 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:23:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:23:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:23:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:23:05 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:23:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b04b6ebe02f61fe28d841f2ba856a1ae79ee9cf1a138d27f051ca0389eda68`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8496aea003fede6970082f61810bf4a3dcb7dce25ca8ccd495549c09ebf3bd56`  
		Last Modified: Tue, 07 Jul 2020 00:25:33 GMT  
		Size: 4.8 MB (4807797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c349cb2025dc596e5bf07c64896c27c193a8b86176d86fa72022dfc0969ea`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 1.3 MB (1326152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cb39cfe1ceb0bb015022053586b49a2dad6b2086d0f1d2cb30431274d6465`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45edddf7821d5f31c4b830e90cb1b347c5d8d3d210fbb9ea3b5b5d260f408ff`  
		Last Modified: Tue, 07 Jul 2020 00:25:32 GMT  
		Size: 929.4 KB (929367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6716b70d2d3b8e2f355a82a2e34d0c70be1a7e1abc7ecbd135d793fe3064ae`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e647ff717838a99fa12f0d6eea2a7952ba37de10c4fcd23df83aeddac61fada`  
		Last Modified: Tue, 07 Jul 2020 00:25:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6143f8fa886d375bf67bfc1ebb4d639a8539258372f5560e5aa7bdd12f282960`  
		Last Modified: Tue, 07 Jul 2020 00:25:45 GMT  
		Size: 75.2 MB (75196357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b866ec661a4ae2a4886cd514e3bb8eddd68a31c9cd2baab2ae5c916e0bcf8c3b`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 4.9 KB (4856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c97cc2dea4fd3440b7fa98bbb890ab824fe2ec15891b864a0d1c9fd366fba7`  
		Last Modified: Tue, 07 Jul 2020 00:25:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7efafa88f0a4c6586e57e6824cb5267da7ae6e1f8a95eb964adfc7f47eac7767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104078223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfdd6ddf350b7108c71ce0f5655da0c603feeb4cca8b99891e3e6b5124f067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:47:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:47:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:47:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:47:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:47:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:48:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:48:12 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:48:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:48:15 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:49:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:49:05 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:49:06 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:49:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:49:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:49:09 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:49:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7906e0fd35e97b195848fbdc84fd0febeedd0ec0381fc2a6cd87a9dddd934`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452177bdbecd5d64e8a6fe94faa2ed568428b54609e8eb4f03385dacbdc38135`  
		Last Modified: Tue, 07 Jul 2020 00:52:50 GMT  
		Size: 4.4 MB (4393243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ef88aeee9b4a526626d68ce7cf72360abd893b3f0423ff429ac0b96ef489e`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 1.3 MB (1262832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd61f4469dbdd0dd87d9c294baa2dbaaaa49e2bfcbec2c4fabdb377ebeeadb`  
		Last Modified: Tue, 07 Jul 2020 00:52:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170407812e234747ee9cc47d200cce9bf4389ad3d731004979b4d55ba6e8e2e1`  
		Last Modified: Tue, 07 Jul 2020 00:52:48 GMT  
		Size: 921.0 KB (920987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2986fa9a28f69bad6c3053bd13e85c905b09b9712611250e5cd848a9a259867`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491fe5a7106bd3fcdf9f4cd8716093c22f9da5b66d285bb95caca2cdec602c3a`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef303867e7f68b8e5c1cddc35fb8ef32c79f9c44d86813fddc3768ad46603f3`  
		Last Modified: Tue, 07 Jul 2020 00:53:10 GMT  
		Size: 73.7 MB (73733057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68561dfc9c7859add2f23eec8b2ce58c2bb6754057dfa0da9ebc4e57adc019b7`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e802a198f6cb745af2ad51bd56d39cd070039b83c12e19a526c8f91f1d2a8`  
		Last Modified: Tue, 07 Jul 2020 00:52:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4b49f54779836d86370dde8a254ea883335d419d83ce9a31336fc6437637e34e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116244732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aee5709104dcc8bb906cc0066469e0159bc71a65a94a361abf5d76bd1659ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:24:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:26:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:26:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:27:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:27:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:27:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:28:02 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:28:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:28:11 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 07 Jul 2020 00:28:13 GMT
ENV MARIADB_VERSION=1:10.2.32+maria~bionic
# Tue, 07 Jul 2020 00:28:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:31:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:31:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:31:19 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:31:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:31:40 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:31:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9180340d63f0c1dfc618663fcfa959d45cfbabda756db268d7258cac2c73b77`  
		Last Modified: Tue, 07 Jul 2020 00:39:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bdc460e1362fd02924ea4b162ed94a50e92fbb16e71dd0aa9860223780d77f`  
		Last Modified: Tue, 07 Jul 2020 00:39:16 GMT  
		Size: 5.6 MB (5628798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d20b021be06a414c9df579d3abde3079e516f2f70d24c5fe3d9d79627e95d0`  
		Last Modified: Tue, 07 Jul 2020 00:39:14 GMT  
		Size: 1.2 MB (1246475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b93237b60bcdea2cd2369671d5f4525a61409096d876659ad07c12a4e645da`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a610689cb6103d9d78be517860a8fd8006f84100c259a6318465a74ccc4a1c7`  
		Last Modified: Tue, 07 Jul 2020 00:39:11 GMT  
		Size: 931.8 KB (931832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef3592d06fb6703b33e2a9e63e22d024a9bf420c5ad6a1ce5bf634b69b8c0c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d98872d26d660f7078455773041269be26171d5608c90029e5a9ff9d42411`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0d0e6ce7eedbc6ab7a7e7a99a52f8a0993ecbf54b755aa4715d825d1390ad3`  
		Last Modified: Tue, 07 Jul 2020 00:39:24 GMT  
		Size: 78.0 MB (77985387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290725b4d016fff7987b6daa3b8718de754675576b668424d04d7150abb2736c`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 4.9 KB (4858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f72ab411730ce6d7fb70a1fdaa64562269c69e72ef3a870464b352cbfa1cf`  
		Last Modified: Tue, 07 Jul 2020 00:39:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:82ea16cdfb9b5702989b8f5297a7b941811ee950bd17651645cd9737fdb92260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:565dc23efd1a83156fbb5f68b090600850419091d7c2e0b825f9a620368d8c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23ebcf1077015c1c2b78868808498fef51eb58f3bb3a714d1c887a5951125e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:21:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:54 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:55 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353e305528eef86ede13fd49689851cfe2780a275359d28fb709f65d1fa7e67`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a9dcb4632b2ceddda187a871ced5a2a9bcaa6005d6af2734514756e7420e4`  
		Last Modified: Tue, 07 Jul 2020 00:25:24 GMT  
		Size: 82.5 MB (82511474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f48d631108907dd12c768764a2f87bdec8912e89abd2ddc10c46f74b4b5cfb`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14acfcd318f1c3ffa64de1d5c7a1b5cdbdf5934660b8a75444d4a643dd31412`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:601a1678564d4641c1a17eaa28a1272055bda1fc2891939161debb309ed16b63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353ff06f180531f43e4d7b13af85c0234529c0d5f8416077931cabab152535b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:45:56 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:45:57 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:45:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:46:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:46:57 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:46:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:46:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:47:01 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:47:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedda6f5d447eb55b7d6ce54d0585c32c5fef3089c6faf24a8ee9c097a946818`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270e3688529bfe977e46e6e0988ae41b4a961186b5f2422329fa3f117000d0cc`  
		Last Modified: Tue, 07 Jul 2020 00:52:38 GMT  
		Size: 81.7 MB (81653939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3007fb2c160f9113a7fdec36a8877d61297d65e547f17c8701570e96b467f3`  
		Last Modified: Tue, 07 Jul 2020 00:52:14 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d5e67a628b1ad9f1eb48ed8cf65b3a2e47d0ac7a98ab20894fa84d9b759e7e`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cef2814eab3924950e05b242388d6f444f95fcebc48f8ffe1472e5635a51744a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129051440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44206289fda10d611bee96cfc5fe1b11c9d3302c8e4e4dbc970ebff3a9533e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:18:22 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:18:29 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:18:38 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83f0a2b65d89970f67a02f1b9e520eda16dcf498bb33f084c102e9b8a61f2b6`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b54cb49dc4090455ce523baca2a6df986a527be644650bbed685682a609d6`  
		Last Modified: Tue, 07 Jul 2020 00:38:44 GMT  
		Size: 86.5 MB (86538734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e25a49acc119ca94f771b1bcad0520210e42fdc1f1f03ad9786d7a3a59dda4`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ddd35597065435ba3c8558bf35fbac75cb350db55520bb136d884d9b87cc35`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23`

```console
$ docker pull mariadb@sha256:82ea16cdfb9b5702989b8f5297a7b941811ee950bd17651645cd9737fdb92260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23` - linux; amd64

```console
$ docker pull mariadb@sha256:565dc23efd1a83156fbb5f68b090600850419091d7c2e0b825f9a620368d8c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23ebcf1077015c1c2b78868808498fef51eb58f3bb3a714d1c887a5951125e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:21:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:54 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:55 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353e305528eef86ede13fd49689851cfe2780a275359d28fb709f65d1fa7e67`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a9dcb4632b2ceddda187a871ced5a2a9bcaa6005d6af2734514756e7420e4`  
		Last Modified: Tue, 07 Jul 2020 00:25:24 GMT  
		Size: 82.5 MB (82511474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f48d631108907dd12c768764a2f87bdec8912e89abd2ddc10c46f74b4b5cfb`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14acfcd318f1c3ffa64de1d5c7a1b5cdbdf5934660b8a75444d4a643dd31412`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:601a1678564d4641c1a17eaa28a1272055bda1fc2891939161debb309ed16b63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353ff06f180531f43e4d7b13af85c0234529c0d5f8416077931cabab152535b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:45:56 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:45:57 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:45:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:46:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:46:57 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:46:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:46:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:47:01 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:47:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedda6f5d447eb55b7d6ce54d0585c32c5fef3089c6faf24a8ee9c097a946818`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270e3688529bfe977e46e6e0988ae41b4a961186b5f2422329fa3f117000d0cc`  
		Last Modified: Tue, 07 Jul 2020 00:52:38 GMT  
		Size: 81.7 MB (81653939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3007fb2c160f9113a7fdec36a8877d61297d65e547f17c8701570e96b467f3`  
		Last Modified: Tue, 07 Jul 2020 00:52:14 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d5e67a628b1ad9f1eb48ed8cf65b3a2e47d0ac7a98ab20894fa84d9b759e7e`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cef2814eab3924950e05b242388d6f444f95fcebc48f8ffe1472e5635a51744a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129051440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44206289fda10d611bee96cfc5fe1b11c9d3302c8e4e4dbc970ebff3a9533e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:18:22 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:18:29 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:18:38 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83f0a2b65d89970f67a02f1b9e520eda16dcf498bb33f084c102e9b8a61f2b6`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b54cb49dc4090455ce523baca2a6df986a527be644650bbed685682a609d6`  
		Last Modified: Tue, 07 Jul 2020 00:38:44 GMT  
		Size: 86.5 MB (86538734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e25a49acc119ca94f771b1bcad0520210e42fdc1f1f03ad9786d7a3a59dda4`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ddd35597065435ba3c8558bf35fbac75cb350db55520bb136d884d9b87cc35`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.23-focal`

```console
$ docker pull mariadb@sha256:82ea16cdfb9b5702989b8f5297a7b941811ee950bd17651645cd9737fdb92260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.23-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:565dc23efd1a83156fbb5f68b090600850419091d7c2e0b825f9a620368d8c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23ebcf1077015c1c2b78868808498fef51eb58f3bb3a714d1c887a5951125e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:21:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:54 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:55 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353e305528eef86ede13fd49689851cfe2780a275359d28fb709f65d1fa7e67`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a9dcb4632b2ceddda187a871ced5a2a9bcaa6005d6af2734514756e7420e4`  
		Last Modified: Tue, 07 Jul 2020 00:25:24 GMT  
		Size: 82.5 MB (82511474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f48d631108907dd12c768764a2f87bdec8912e89abd2ddc10c46f74b4b5cfb`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14acfcd318f1c3ffa64de1d5c7a1b5cdbdf5934660b8a75444d4a643dd31412`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:601a1678564d4641c1a17eaa28a1272055bda1fc2891939161debb309ed16b63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353ff06f180531f43e4d7b13af85c0234529c0d5f8416077931cabab152535b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:45:56 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:45:57 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:45:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:46:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:46:57 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:46:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:46:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:47:01 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:47:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedda6f5d447eb55b7d6ce54d0585c32c5fef3089c6faf24a8ee9c097a946818`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270e3688529bfe977e46e6e0988ae41b4a961186b5f2422329fa3f117000d0cc`  
		Last Modified: Tue, 07 Jul 2020 00:52:38 GMT  
		Size: 81.7 MB (81653939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3007fb2c160f9113a7fdec36a8877d61297d65e547f17c8701570e96b467f3`  
		Last Modified: Tue, 07 Jul 2020 00:52:14 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d5e67a628b1ad9f1eb48ed8cf65b3a2e47d0ac7a98ab20894fa84d9b759e7e`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.23-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cef2814eab3924950e05b242388d6f444f95fcebc48f8ffe1472e5635a51744a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129051440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44206289fda10d611bee96cfc5fe1b11c9d3302c8e4e4dbc970ebff3a9533e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:18:22 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:18:29 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:18:38 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83f0a2b65d89970f67a02f1b9e520eda16dcf498bb33f084c102e9b8a61f2b6`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b54cb49dc4090455ce523baca2a6df986a527be644650bbed685682a609d6`  
		Last Modified: Tue, 07 Jul 2020 00:38:44 GMT  
		Size: 86.5 MB (86538734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e25a49acc119ca94f771b1bcad0520210e42fdc1f1f03ad9786d7a3a59dda4`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ddd35597065435ba3c8558bf35fbac75cb350db55520bb136d884d9b87cc35`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:82ea16cdfb9b5702989b8f5297a7b941811ee950bd17651645cd9737fdb92260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:565dc23efd1a83156fbb5f68b090600850419091d7c2e0b825f9a620368d8c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23ebcf1077015c1c2b78868808498fef51eb58f3bb3a714d1c887a5951125e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:21:27 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:21:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:54 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:55 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353e305528eef86ede13fd49689851cfe2780a275359d28fb709f65d1fa7e67`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a9dcb4632b2ceddda187a871ced5a2a9bcaa6005d6af2734514756e7420e4`  
		Last Modified: Tue, 07 Jul 2020 00:25:24 GMT  
		Size: 82.5 MB (82511474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f48d631108907dd12c768764a2f87bdec8912e89abd2ddc10c46f74b4b5cfb`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14acfcd318f1c3ffa64de1d5c7a1b5cdbdf5934660b8a75444d4a643dd31412`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:601a1678564d4641c1a17eaa28a1272055bda1fc2891939161debb309ed16b63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353ff06f180531f43e4d7b13af85c0234529c0d5f8416077931cabab152535b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:45:56 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:45:57 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:45:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:46:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:46:57 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:46:58 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:46:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:47:01 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:47:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedda6f5d447eb55b7d6ce54d0585c32c5fef3089c6faf24a8ee9c097a946818`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270e3688529bfe977e46e6e0988ae41b4a961186b5f2422329fa3f117000d0cc`  
		Last Modified: Tue, 07 Jul 2020 00:52:38 GMT  
		Size: 81.7 MB (81653939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3007fb2c160f9113a7fdec36a8877d61297d65e547f17c8701570e96b467f3`  
		Last Modified: Tue, 07 Jul 2020 00:52:14 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d5e67a628b1ad9f1eb48ed8cf65b3a2e47d0ac7a98ab20894fa84d9b759e7e`  
		Last Modified: Tue, 07 Jul 2020 00:52:13 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cef2814eab3924950e05b242388d6f444f95fcebc48f8ffe1472e5635a51744a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129051440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44206289fda10d611bee96cfc5fe1b11c9d3302c8e4e4dbc970ebff3a9533e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:18:22 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 07 Jul 2020 00:18:29 GMT
ENV MARIADB_VERSION=1:10.3.23+maria~focal
# Tue, 07 Jul 2020 00:18:38 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:23:50 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:24:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:24:04 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:24:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:24:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:24:21 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:24:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83f0a2b65d89970f67a02f1b9e520eda16dcf498bb33f084c102e9b8a61f2b6`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b54cb49dc4090455ce523baca2a6df986a527be644650bbed685682a609d6`  
		Last Modified: Tue, 07 Jul 2020 00:38:44 GMT  
		Size: 86.5 MB (86538734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e25a49acc119ca94f771b1bcad0520210e42fdc1f1f03ad9786d7a3a59dda4`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ddd35597065435ba3c8558bf35fbac75cb350db55520bb136d884d9b87cc35`  
		Last Modified: Tue, 07 Jul 2020 00:38:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:b5b4c6dad0f9b955d711fb2b389523ee29094b7cc6f11d85002edb1351f80416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:2ff6d9c2592d54cd06ae96c7f3af4f2e05c722a292a7aa7ac74d477053327085
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123547829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc594751fe2aa4b157a9525bcec3451d83c0becd3749adf1ce4e17ea595bea6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:20:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:22 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac421ade4a106aa3d8d4532e007263472ff03bb4c95d694481aa9075316685`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1a2b92cb7b12162a164285ef69fe3ca83898e4871eeb889c5952515bf7e58`  
		Last Modified: Tue, 07 Jul 2020 00:25:01 GMT  
		Size: 86.9 MB (86869194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c9614e2309154966316ff86862a063a794ac0ef91c32aa58f610974a35e4c`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929db88c4deceb75062d2b269d6315650c10ba4673b25d467a7ffbb1929123e5`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e1d95654b5716e3c49d0063125d6e30fbad2908d74a08bcde3de91a5efebec66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121142008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b72f1f15760617f16e6e4f5b48d0a40c36eafa45bdc4e3b978bf14cd5a551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:45:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:45:39 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:45:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:45:42 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:45:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:45:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:45:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dfba146502304821d37814ea33005e5b7f1f4557ca5e20bf709ba82a76e8a5`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63885acc1ce8df1f344e7cd49365f145bea896de6ced36dc1032fab2b6b9a4`  
		Last Modified: Tue, 07 Jul 2020 00:52:02 GMT  
		Size: 86.0 MB (85958712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7809be1591c52e7f7d3107e82348ce0119081fb485d774014d41c1391e10f334`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd23ee6e4f4af5606dfb6195bc6dfe3299e970b6ee82c56e4cafb24201dc955f`  
		Last Modified: Tue, 07 Jul 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:81fd17f20c894b348a7758dad821c97f1dfb998cda5c3fd7ac3f7bca44d39faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18b2aca2c4858d4d722fbfd62e0e509214e7efc714b00a3d486b038c479f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:11:04 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:11:07 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:11:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:17:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:17:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:17:28 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:17:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:17:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:57 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:18:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5cfc98c2f4947da3fa82f4b027c8074deffaf833f162d7faaed0ae1268bad`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c372108337e20b323ad7f6cdf1046a1eab0ac16e6ae21c1309dc5f2308cab581`  
		Last Modified: Tue, 07 Jul 2020 00:38:01 GMT  
		Size: 91.0 MB (90988277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96078772a4979954958fbe8d4809f75e24ec8e82238b86de43a47ffe9d6e7770`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d370af35884d99b1eba62d4e361010333ba9d5be3347892303c0bcf837b463eb`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13`

```console
$ docker pull mariadb@sha256:b5b4c6dad0f9b955d711fb2b389523ee29094b7cc6f11d85002edb1351f80416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13` - linux; amd64

```console
$ docker pull mariadb@sha256:2ff6d9c2592d54cd06ae96c7f3af4f2e05c722a292a7aa7ac74d477053327085
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123547829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc594751fe2aa4b157a9525bcec3451d83c0becd3749adf1ce4e17ea595bea6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:20:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:22 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac421ade4a106aa3d8d4532e007263472ff03bb4c95d694481aa9075316685`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1a2b92cb7b12162a164285ef69fe3ca83898e4871eeb889c5952515bf7e58`  
		Last Modified: Tue, 07 Jul 2020 00:25:01 GMT  
		Size: 86.9 MB (86869194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c9614e2309154966316ff86862a063a794ac0ef91c32aa58f610974a35e4c`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929db88c4deceb75062d2b269d6315650c10ba4673b25d467a7ffbb1929123e5`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e1d95654b5716e3c49d0063125d6e30fbad2908d74a08bcde3de91a5efebec66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121142008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b72f1f15760617f16e6e4f5b48d0a40c36eafa45bdc4e3b978bf14cd5a551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:45:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:45:39 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:45:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:45:42 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:45:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:45:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:45:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dfba146502304821d37814ea33005e5b7f1f4557ca5e20bf709ba82a76e8a5`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63885acc1ce8df1f344e7cd49365f145bea896de6ced36dc1032fab2b6b9a4`  
		Last Modified: Tue, 07 Jul 2020 00:52:02 GMT  
		Size: 86.0 MB (85958712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7809be1591c52e7f7d3107e82348ce0119081fb485d774014d41c1391e10f334`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd23ee6e4f4af5606dfb6195bc6dfe3299e970b6ee82c56e4cafb24201dc955f`  
		Last Modified: Tue, 07 Jul 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:81fd17f20c894b348a7758dad821c97f1dfb998cda5c3fd7ac3f7bca44d39faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18b2aca2c4858d4d722fbfd62e0e509214e7efc714b00a3d486b038c479f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:11:04 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:11:07 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:11:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:17:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:17:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:17:28 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:17:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:17:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:57 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:18:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5cfc98c2f4947da3fa82f4b027c8074deffaf833f162d7faaed0ae1268bad`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c372108337e20b323ad7f6cdf1046a1eab0ac16e6ae21c1309dc5f2308cab581`  
		Last Modified: Tue, 07 Jul 2020 00:38:01 GMT  
		Size: 91.0 MB (90988277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96078772a4979954958fbe8d4809f75e24ec8e82238b86de43a47ffe9d6e7770`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d370af35884d99b1eba62d4e361010333ba9d5be3347892303c0bcf837b463eb`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.13-focal`

```console
$ docker pull mariadb@sha256:b5b4c6dad0f9b955d711fb2b389523ee29094b7cc6f11d85002edb1351f80416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2ff6d9c2592d54cd06ae96c7f3af4f2e05c722a292a7aa7ac74d477053327085
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123547829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc594751fe2aa4b157a9525bcec3451d83c0becd3749adf1ce4e17ea595bea6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:20:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:22 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac421ade4a106aa3d8d4532e007263472ff03bb4c95d694481aa9075316685`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1a2b92cb7b12162a164285ef69fe3ca83898e4871eeb889c5952515bf7e58`  
		Last Modified: Tue, 07 Jul 2020 00:25:01 GMT  
		Size: 86.9 MB (86869194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c9614e2309154966316ff86862a063a794ac0ef91c32aa58f610974a35e4c`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929db88c4deceb75062d2b269d6315650c10ba4673b25d467a7ffbb1929123e5`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e1d95654b5716e3c49d0063125d6e30fbad2908d74a08bcde3de91a5efebec66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121142008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b72f1f15760617f16e6e4f5b48d0a40c36eafa45bdc4e3b978bf14cd5a551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:45:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:45:39 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:45:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:45:42 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:45:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:45:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:45:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dfba146502304821d37814ea33005e5b7f1f4557ca5e20bf709ba82a76e8a5`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63885acc1ce8df1f344e7cd49365f145bea896de6ced36dc1032fab2b6b9a4`  
		Last Modified: Tue, 07 Jul 2020 00:52:02 GMT  
		Size: 86.0 MB (85958712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7809be1591c52e7f7d3107e82348ce0119081fb485d774014d41c1391e10f334`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd23ee6e4f4af5606dfb6195bc6dfe3299e970b6ee82c56e4cafb24201dc955f`  
		Last Modified: Tue, 07 Jul 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:81fd17f20c894b348a7758dad821c97f1dfb998cda5c3fd7ac3f7bca44d39faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18b2aca2c4858d4d722fbfd62e0e509214e7efc714b00a3d486b038c479f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:11:04 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:11:07 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:11:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:17:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:17:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:17:28 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:17:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:17:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:57 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:18:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5cfc98c2f4947da3fa82f4b027c8074deffaf833f162d7faaed0ae1268bad`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c372108337e20b323ad7f6cdf1046a1eab0ac16e6ae21c1309dc5f2308cab581`  
		Last Modified: Tue, 07 Jul 2020 00:38:01 GMT  
		Size: 91.0 MB (90988277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96078772a4979954958fbe8d4809f75e24ec8e82238b86de43a47ffe9d6e7770`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d370af35884d99b1eba62d4e361010333ba9d5be3347892303c0bcf837b463eb`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:b5b4c6dad0f9b955d711fb2b389523ee29094b7cc6f11d85002edb1351f80416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2ff6d9c2592d54cd06ae96c7f3af4f2e05c722a292a7aa7ac74d477053327085
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123547829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc594751fe2aa4b157a9525bcec3451d83c0becd3749adf1ce4e17ea595bea6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:20:58 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:20:59 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:21:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:21:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:21:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:21:22 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:21:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac421ade4a106aa3d8d4532e007263472ff03bb4c95d694481aa9075316685`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1a2b92cb7b12162a164285ef69fe3ca83898e4871eeb889c5952515bf7e58`  
		Last Modified: Tue, 07 Jul 2020 00:25:01 GMT  
		Size: 86.9 MB (86869194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c9614e2309154966316ff86862a063a794ac0ef91c32aa58f610974a35e4c`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 4.9 KB (4854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929db88c4deceb75062d2b269d6315650c10ba4673b25d467a7ffbb1929123e5`  
		Last Modified: Tue, 07 Jul 2020 00:24:46 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e1d95654b5716e3c49d0063125d6e30fbad2908d74a08bcde3de91a5efebec66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121142008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b72f1f15760617f16e6e4f5b48d0a40c36eafa45bdc4e3b978bf14cd5a551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:44:59 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:45:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:45:39 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:45:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:45:42 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:45:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:45:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:45:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dfba146502304821d37814ea33005e5b7f1f4557ca5e20bf709ba82a76e8a5`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63885acc1ce8df1f344e7cd49365f145bea896de6ced36dc1032fab2b6b9a4`  
		Last Modified: Tue, 07 Jul 2020 00:52:02 GMT  
		Size: 86.0 MB (85958712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7809be1591c52e7f7d3107e82348ce0119081fb485d774014d41c1391e10f334`  
		Last Modified: Tue, 07 Jul 2020 00:51:36 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd23ee6e4f4af5606dfb6195bc6dfe3299e970b6ee82c56e4cafb24201dc955f`  
		Last Modified: Tue, 07 Jul 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:81fd17f20c894b348a7758dad821c97f1dfb998cda5c3fd7ac3f7bca44d39faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18b2aca2c4858d4d722fbfd62e0e509214e7efc714b00a3d486b038c479f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:11:04 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 07 Jul 2020 00:11:07 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Tue, 07 Jul 2020 00:11:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:17:15 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:17:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:17:28 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:17:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 07 Jul 2020 00:17:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:57 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:18:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5cfc98c2f4947da3fa82f4b027c8074deffaf833f162d7faaed0ae1268bad`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c372108337e20b323ad7f6cdf1046a1eab0ac16e6ae21c1309dc5f2308cab581`  
		Last Modified: Tue, 07 Jul 2020 00:38:01 GMT  
		Size: 91.0 MB (90988277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96078772a4979954958fbe8d4809f75e24ec8e82238b86de43a47ffe9d6e7770`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 4.9 KB (4857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d370af35884d99b1eba62d4e361010333ba9d5be3347892303c0bcf837b463eb`  
		Last Modified: Tue, 07 Jul 2020 00:37:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.4`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.4` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.4-focal`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:a317e3553e49f718a462f544cfc0ad9f83d705667f73dd9dc774515c338c547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:86e368b140a863112799c1f366fd04172733dc440353e9334007ea9f37a9b3db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125502162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c380b0dd8c8a0846c6cfbc16ef9c1a8019e85377b2b99e5d393746d2bc611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:19:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:20:01 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:20:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:20:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:20:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:20:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:20:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:20:17 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:20:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:20:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:20:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:20:46 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:20:46 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:20:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd31a8b718ff2876d5c8eb31c0f8dd65c78f0c14be49d7f0ff0521504d81ecc`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03768a32e57b6f55e96471f19867cdd714762eb671ca1d6c1e4001f3fcc313a`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 5.5 MB (5490581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4ef2ecadfeb294ad36d514ad23cb73738991641f3c4a8732215c6fef08c73c`  
		Last Modified: Tue, 07 Jul 2020 00:24:23 GMT  
		Size: 1.3 MB (1323238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c98359f80216eb0485fe0d5ec68a3c2a6f018b727eb3d34f4dc4a3f880a1`  
		Last Modified: Tue, 07 Jul 2020 00:24:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4296564e05a3f045b7e7dd554d9454a8032f8e9a8c09d4dec1ed70f134c12c7`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 1.3 MB (1265072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed3238308db09981912551c0ec327102db83a292b00b5b720c3552395206d86`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1a5c858173d8072128656993e652d44333dff77b81b2f2794b31b0cbc8fb8`  
		Last Modified: Tue, 07 Jul 2020 00:24:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3212c3b29b8fdb97b5b83c75d2427e8d2b5afe2c1ba65599ae2186f3ec91aa`  
		Last Modified: Tue, 07 Jul 2020 00:24:37 GMT  
		Size: 88.8 MB (88823646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034e7ff7d232b03b87fb20ddbd63a1067c0261ee0a5f2cad457f91e86101e9`  
		Last Modified: Tue, 07 Jul 2020 00:24:20 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:23f527b8a74be922e8e79b21c7c9e3c69df65c81617861f3a8975d7544f57ef4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123135482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07b188bcfdd3a6e7f3e8de14920304fef4ba29cf216a1a456c734b73136f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:43:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:43:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:43:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:43:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:43:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:44:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:44:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:44:03 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:44:04 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:44:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:44:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:44:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:44:47 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:44:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:44:49 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:44:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06a2923b3833e90279c7485ef795f7bf73fa4c00004d2c46faad19c2fdce2b`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2e995e0e8d60a4526a58003bb90247fea4cc24881c848ce82f1180710166f`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 5.5 MB (5457480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5307830a2e99c66f43012914059339198b5e45019faf1e8693290b0b9b5208aa`  
		Last Modified: Tue, 07 Jul 2020 00:50:58 GMT  
		Size: 1.3 MB (1259499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f15d8b66d03b3e3be63a11757c7df944429af1dbf388c70c762fa3791c7f1`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3d186487b146fa6e79aeef8c565d3fb72ab7d5255f0dc2da2a17950ed9044`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 1.3 MB (1263857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994914027af888d1b03852f84803a8f6a6348a703d3467b77ee1e563cf9ca862`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240e1aef2d959d5a071a74943d89bd254eee4c8c0b6e64a61fea4e52058f15d`  
		Last Modified: Tue, 07 Jul 2020 00:50:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61770237350613be1fd6424f814ec77a95afc08e412827b1da87c0e6a6b9e64`  
		Last Modified: Tue, 07 Jul 2020 00:51:21 GMT  
		Size: 88.0 MB (87952306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7920c41ddc80590f6d33b3202e53ac886a68e789bfb05c19fb667ce9376aecd`  
		Last Modified: Tue, 07 Jul 2020 00:50:55 GMT  
		Size: 4.9 KB (4853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91db220bafabc5b2666677124be1ceaab496ef89c214a6ac209fd15946c3a5e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135518833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd491c083289f1b40f7dd4d07dedb37d882f974aba26c757b52d8166d8f6a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Jul 2020 22:13:24 GMT
ADD file:527b698ef39c198d3bb4f261436fc117e0bfbacb823a8e68a25a7645de644f32 in / 
# Mon, 06 Jul 2020 22:13:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:13:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:14:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:14:15 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:00:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 07 Jul 2020 00:02:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:02:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jul 2020 00:03:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jul 2020 00:04:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jul 2020 00:04:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:05:06 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 07 Jul 2020 00:05:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 07 Jul 2020 00:05:26 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 07 Jul 2020 00:05:34 GMT
ENV MARIADB_VERSION=1:10.5.4+maria~focal
# Tue, 07 Jul 2020 00:05:51 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 07 Jul 2020 00:10:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 07 Jul 2020 00:10:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Jul 2020 00:10:26 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:10:39 GMT
EXPOSE 3306
# Tue, 07 Jul 2020 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:78dd70c068997cdafbab6bdae26eb64e19778a9b8b1cb8cf8ff968b9194ed1d7`  
		Last Modified: Mon, 06 Jul 2020 15:50:38 GMT  
		Size: 33.3 MB (33278868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743c07d6617b50bc142b1d300e49a94499fd97eabcc659ed83b70195860bb0ad`  
		Last Modified: Mon, 06 Jul 2020 22:18:24 GMT  
		Size: 32.2 KB (32161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f7d135960a9bb461819ec0585556bdf31a5d529a0a2be90e319d8b22c36b3f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a570a4ab9de9300dfbc146a34311e197808dd24282d6547211269df5abee98f`  
		Last Modified: Mon, 06 Jul 2020 22:18:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3d7637716e212bb5511a5b0f170ee5af1f4b747a047fc58d2839c05b0f60d`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1356960992be81f8d7e52c95338264774221c496a3d4bdb1feb8d740ef105a`  
		Last Modified: Tue, 07 Jul 2020 00:36:55 GMT  
		Size: 6.7 MB (6671923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e9a9c4541c9e06345c92d23613d92c9d76ff3f1b219a3d4498ece517016e3f`  
		Last Modified: Tue, 07 Jul 2020 00:36:54 GMT  
		Size: 1.2 MB (1242875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67965210847561623af4fe04da654864efa86c647a354c048b30594bf5dbb90b`  
		Last Modified: Tue, 07 Jul 2020 00:36:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96776c3fd8fb72327ce58dc923e4f0a9202be644adc34d19e49a9817d40391`  
		Last Modified: Tue, 07 Jul 2020 00:36:50 GMT  
		Size: 1.3 MB (1276136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba79c9f15c83fc87408d6dc20371ec0782441bbbb29e10ac2d586a3632f905c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465310afd92e9302f6e4bac442e0547bedf8dbb0eed16522b31c7cc7987ae26e`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c7e7a1524081d15635b5dcf9b0fb07b57c63c301cd49eafcacd35f61cf15d8`  
		Last Modified: Tue, 07 Jul 2020 00:37:12 GMT  
		Size: 93.0 MB (93006248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2ecbc8ef8ec345843f645aea00863f6d43dd9bfeebd5f02eea2b1f9bcbf4c`  
		Last Modified: Tue, 07 Jul 2020 00:36:49 GMT  
		Size: 4.9 KB (4855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
