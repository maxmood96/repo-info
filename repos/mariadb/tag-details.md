<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10.1`](#mariadb101)
-	[`mariadb:10.1.48`](#mariadb10148)
-	[`mariadb:10.1.48-bionic`](#mariadb10148-bionic)
-	[`mariadb:10.1-bionic`](#mariadb101-bionic)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2.37`](#mariadb10237)
-	[`mariadb:10.2.37-bionic`](#mariadb10237-bionic)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3.28`](#mariadb10328)
-	[`mariadb:10.3.28-focal`](#mariadb10328-focal)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4.18`](#mariadb10418)
-	[`mariadb:10.4.18-focal`](#mariadb10418-focal)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5.9`](#mariadb1059)
-	[`mariadb:10.5.9-focal`](#mariadb1059-focal)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1`

```console
$ docker pull mariadb@sha256:3ad3b52f0e0fcdee3204072981d4c4df29ff9d2b6bb3a7c6a2b6089805325c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1` - linux; amd64

```console
$ docker pull mariadb@sha256:9139f98a7fc54edb2020151dca409ba4052981d18c393074da6d6ea60b831c6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113180207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2fed152fe12cbc1e1adbebcc89035df6f230b7c0c0c955c90827826e3bdf59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 04:32:33 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:33:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:33:06 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:33:06 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:33:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:33:08 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:33:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b7d8813e0e076ed8cfee13a9c3ddf295ee56ca35f50304160a3a76fd58b31`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b4d64470cd558b877e43684728e1dd8d378c9af8d9f35d82a66e6c916acaf`  
		Last Modified: Thu, 04 Mar 2021 04:35:11 GMT  
		Size: 79.4 MB (79382116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9fec02a8467f6e79b5ad9d18ec1f902c84bafdaae3d74c77f757a034a490d1`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384af7d60a0ab371150bc38d9e4dc4d09b07af23403be9e02f3eab35476594da`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b3588677e67506764d3f3718584ddb41011841753f763e7600dd1ceb321e73e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105801913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2512b6b4ad3802feff734b443cd262a86beb7e625bdea96e77512dd9353ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:12:15 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 05:12:16 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 05:12:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:13:05 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:13:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:13:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:13:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:13:12 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:13:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e809ddb10e00c12a15b768c701b5465471f4fb0d8a6bf1d72dad172a0083b71`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751390edf4a14d86e650a0c4b509af6bba4d50483e9647912285cbfce397da40`  
		Last Modified: Thu, 04 Mar 2021 05:16:19 GMT  
		Size: 75.5 MB (75471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8160fb8118add24b53b133500e0d0914a536aaecd2cf3e724a5a625a1d9e3`  
		Last Modified: Thu, 04 Mar 2021 05:15:59 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0262a98fc8c7bd894fa14502b2b247a87d06aee24f4dfd082de113e1741ba61a`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd3211ab60016b5fbad67eefea97cb8b74e65ac98b3d1568e56c666f8a37f125
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118170783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5554bc1085f06beeab6885bd130b267cb25e5084c00520678c876afcce8c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:47:05 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 06:47:12 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 06:47:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:52:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:52:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:52:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:53:21 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:53:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5a39539e36cc64214bacaafd3e57dba1ec0baa41e6f688bfd642cc7d266a7`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d52e15224ea8409ca9abafd51bdb4d63c7069bf938bb8bd672891986b2e9ff`  
		Last Modified: Thu, 04 Mar 2021 06:57:25 GMT  
		Size: 79.9 MB (79923768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b04d249d143967eab626ef745f88b2ce5409ea97e40d7cc23319b00379685d`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e5137285d83769e26a4b0c228b4f910bea26f4ca8dece1bcb70f5b5d53434`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.48`

```console
$ docker pull mariadb@sha256:3ad3b52f0e0fcdee3204072981d4c4df29ff9d2b6bb3a7c6a2b6089805325c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.48` - linux; amd64

```console
$ docker pull mariadb@sha256:9139f98a7fc54edb2020151dca409ba4052981d18c393074da6d6ea60b831c6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113180207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2fed152fe12cbc1e1adbebcc89035df6f230b7c0c0c955c90827826e3bdf59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 04:32:33 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:33:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:33:06 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:33:06 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:33:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:33:08 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:33:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b7d8813e0e076ed8cfee13a9c3ddf295ee56ca35f50304160a3a76fd58b31`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b4d64470cd558b877e43684728e1dd8d378c9af8d9f35d82a66e6c916acaf`  
		Last Modified: Thu, 04 Mar 2021 04:35:11 GMT  
		Size: 79.4 MB (79382116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9fec02a8467f6e79b5ad9d18ec1f902c84bafdaae3d74c77f757a034a490d1`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384af7d60a0ab371150bc38d9e4dc4d09b07af23403be9e02f3eab35476594da`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.48` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b3588677e67506764d3f3718584ddb41011841753f763e7600dd1ceb321e73e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105801913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2512b6b4ad3802feff734b443cd262a86beb7e625bdea96e77512dd9353ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:12:15 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 05:12:16 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 05:12:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:13:05 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:13:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:13:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:13:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:13:12 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:13:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e809ddb10e00c12a15b768c701b5465471f4fb0d8a6bf1d72dad172a0083b71`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751390edf4a14d86e650a0c4b509af6bba4d50483e9647912285cbfce397da40`  
		Last Modified: Thu, 04 Mar 2021 05:16:19 GMT  
		Size: 75.5 MB (75471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8160fb8118add24b53b133500e0d0914a536aaecd2cf3e724a5a625a1d9e3`  
		Last Modified: Thu, 04 Mar 2021 05:15:59 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0262a98fc8c7bd894fa14502b2b247a87d06aee24f4dfd082de113e1741ba61a`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.48` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd3211ab60016b5fbad67eefea97cb8b74e65ac98b3d1568e56c666f8a37f125
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118170783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5554bc1085f06beeab6885bd130b267cb25e5084c00520678c876afcce8c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:47:05 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 06:47:12 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 06:47:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:52:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:52:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:52:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:53:21 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:53:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5a39539e36cc64214bacaafd3e57dba1ec0baa41e6f688bfd642cc7d266a7`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d52e15224ea8409ca9abafd51bdb4d63c7069bf938bb8bd672891986b2e9ff`  
		Last Modified: Thu, 04 Mar 2021 06:57:25 GMT  
		Size: 79.9 MB (79923768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b04d249d143967eab626ef745f88b2ce5409ea97e40d7cc23319b00379685d`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e5137285d83769e26a4b0c228b4f910bea26f4ca8dece1bcb70f5b5d53434`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1.48-bionic`

```console
$ docker pull mariadb@sha256:3ad3b52f0e0fcdee3204072981d4c4df29ff9d2b6bb3a7c6a2b6089805325c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1.48-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:9139f98a7fc54edb2020151dca409ba4052981d18c393074da6d6ea60b831c6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113180207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2fed152fe12cbc1e1adbebcc89035df6f230b7c0c0c955c90827826e3bdf59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 04:32:33 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:33:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:33:06 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:33:06 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:33:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:33:08 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:33:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b7d8813e0e076ed8cfee13a9c3ddf295ee56ca35f50304160a3a76fd58b31`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b4d64470cd558b877e43684728e1dd8d378c9af8d9f35d82a66e6c916acaf`  
		Last Modified: Thu, 04 Mar 2021 04:35:11 GMT  
		Size: 79.4 MB (79382116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9fec02a8467f6e79b5ad9d18ec1f902c84bafdaae3d74c77f757a034a490d1`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384af7d60a0ab371150bc38d9e4dc4d09b07af23403be9e02f3eab35476594da`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.48-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b3588677e67506764d3f3718584ddb41011841753f763e7600dd1ceb321e73e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105801913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2512b6b4ad3802feff734b443cd262a86beb7e625bdea96e77512dd9353ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:12:15 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 05:12:16 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 05:12:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:13:05 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:13:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:13:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:13:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:13:12 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:13:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e809ddb10e00c12a15b768c701b5465471f4fb0d8a6bf1d72dad172a0083b71`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751390edf4a14d86e650a0c4b509af6bba4d50483e9647912285cbfce397da40`  
		Last Modified: Thu, 04 Mar 2021 05:16:19 GMT  
		Size: 75.5 MB (75471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8160fb8118add24b53b133500e0d0914a536aaecd2cf3e724a5a625a1d9e3`  
		Last Modified: Thu, 04 Mar 2021 05:15:59 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0262a98fc8c7bd894fa14502b2b247a87d06aee24f4dfd082de113e1741ba61a`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1.48-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd3211ab60016b5fbad67eefea97cb8b74e65ac98b3d1568e56c666f8a37f125
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118170783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5554bc1085f06beeab6885bd130b267cb25e5084c00520678c876afcce8c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:47:05 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 06:47:12 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 06:47:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:52:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:52:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:52:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:53:21 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:53:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5a39539e36cc64214bacaafd3e57dba1ec0baa41e6f688bfd642cc7d266a7`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d52e15224ea8409ca9abafd51bdb4d63c7069bf938bb8bd672891986b2e9ff`  
		Last Modified: Thu, 04 Mar 2021 06:57:25 GMT  
		Size: 79.9 MB (79923768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b04d249d143967eab626ef745f88b2ce5409ea97e40d7cc23319b00379685d`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e5137285d83769e26a4b0c228b4f910bea26f4ca8dece1bcb70f5b5d53434`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.1-bionic`

```console
$ docker pull mariadb@sha256:3ad3b52f0e0fcdee3204072981d4c4df29ff9d2b6bb3a7c6a2b6089805325c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.1-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:9139f98a7fc54edb2020151dca409ba4052981d18c393074da6d6ea60b831c6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113180207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2fed152fe12cbc1e1adbebcc89035df6f230b7c0c0c955c90827826e3bdf59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 04:32:32 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 04:32:33 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:33:06 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:33:06 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:33:06 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:33:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:33:08 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:33:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b7d8813e0e076ed8cfee13a9c3ddf295ee56ca35f50304160a3a76fd58b31`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b4d64470cd558b877e43684728e1dd8d378c9af8d9f35d82a66e6c916acaf`  
		Last Modified: Thu, 04 Mar 2021 04:35:11 GMT  
		Size: 79.4 MB (79382116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9fec02a8467f6e79b5ad9d18ec1f902c84bafdaae3d74c77f757a034a490d1`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384af7d60a0ab371150bc38d9e4dc4d09b07af23403be9e02f3eab35476594da`  
		Last Modified: Thu, 04 Mar 2021 04:34:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b3588677e67506764d3f3718584ddb41011841753f763e7600dd1ceb321e73e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105801913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2512b6b4ad3802feff734b443cd262a86beb7e625bdea96e77512dd9353ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:12:15 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 05:12:16 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 05:12:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:13:05 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:13:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:13:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:13:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:13:12 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:13:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e809ddb10e00c12a15b768c701b5465471f4fb0d8a6bf1d72dad172a0083b71`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751390edf4a14d86e650a0c4b509af6bba4d50483e9647912285cbfce397da40`  
		Last Modified: Thu, 04 Mar 2021 05:16:19 GMT  
		Size: 75.5 MB (75471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8160fb8118add24b53b133500e0d0914a536aaecd2cf3e724a5a625a1d9e3`  
		Last Modified: Thu, 04 Mar 2021 05:15:59 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0262a98fc8c7bd894fa14502b2b247a87d06aee24f4dfd082de113e1741ba61a`  
		Last Modified: Thu, 04 Mar 2021 05:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.1-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd3211ab60016b5fbad67eefea97cb8b74e65ac98b3d1568e56c666f8a37f125
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118170783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5554bc1085f06beeab6885bd130b267cb25e5084c00520678c876afcce8c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:47:05 GMT
ENV MARIADB_MAJOR=10.1
# Thu, 04 Mar 2021 06:47:12 GMT
ENV MARIADB_VERSION=1:10.1.48+maria-1~bionic
# Thu, 04 Mar 2021 06:47:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:52:38 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.1 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:52:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:52:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:53:21 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:53:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5a39539e36cc64214bacaafd3e57dba1ec0baa41e6f688bfd642cc7d266a7`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d52e15224ea8409ca9abafd51bdb4d63c7069bf938bb8bd672891986b2e9ff`  
		Last Modified: Thu, 04 Mar 2021 06:57:25 GMT  
		Size: 79.9 MB (79923768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b04d249d143967eab626ef745f88b2ce5409ea97e40d7cc23319b00379685d`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e5137285d83769e26a4b0c228b4f910bea26f4ca8dece1bcb70f5b5d53434`  
		Last Modified: Thu, 04 Mar 2021 06:57:08 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:8a438741fde0e57870131c7641aa9fd806157bde3971768daa10779c21a9ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:439b0f747583815a1b19bf6bbb021f572d512b5e7b7f8ead02efa6f56ca2709b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107994969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ea9f3c9867ea2da7cef023c8c2635fd5307c8aa494870c2ab9770f171143c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 04:31:46 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:32:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:32:18 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:32:18 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:32:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:32:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:32:19 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f2d0ff8f45d43dffd1135bda5a1dc7105de6ddf9bf9a9ed5e4bddb84f137f`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ca81f3f39b625e126d993555a098320bbae31fe0b4ff49ee83663d35662ff`  
		Last Modified: Thu, 04 Mar 2021 04:34:51 GMT  
		Size: 74.2 MB (74196878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee9bfeecca0b294ed9602c569c4fbc00c83187f8fe7c918a9fc0bf0b54ac025`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54099fae91675f0a37ebbd7b729d527fdbf8f0726c7850b50b78eef1fb777fbc`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:41e0b44b138e68dff225a31d162581175d4a900753dd6ec0ca3d175e156b23f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103141928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e10db427fd771b9c53b44b2b080f88ab5fb0ef3db5afff19bf1e338c8f80f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:11:07 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 05:11:08 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 05:11:10 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:11:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:11:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:11:52 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:11:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:11:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:11:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59d5168fcca261f6c64f3e7c589f45639812c32e8faad9e393c2d9d5eee3ebd`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47601255f2573ec41073df7102597f8ebb232d95034e9cc508fe57cbb529cf41`  
		Last Modified: Thu, 04 Mar 2021 05:15:49 GMT  
		Size: 72.8 MB (72811904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e95411cf8aad99aa40fbbfffea2ab171af3290807f90265f377ba1b6daad4`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e241069f86657853a4833dd08af7b6d75d5e8aaa8e1af424246d0ee08fcbc`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6f9c8f2dba5b006608bd11c44a7dc321c98028c731a4a09eb1938053ce103719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca52c5eab0773f9a18fa387b3573b90662f2498d00a7afd1a115699e0d4e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:41:58 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 06:42:07 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 06:42:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:46:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:46:17 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:46:19 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:46:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:46:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:46:45 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:46:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997301be2225c5dd5af97c84c36ea5eeb7b94dad8578e61b792a791538d8ed5d`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfa86a6fdedeff2832388e3cba3b6c711584f861e46280359018eacc99c407a`  
		Last Modified: Thu, 04 Mar 2021 06:56:46 GMT  
		Size: 77.8 MB (77768320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab67bd3f9ac2a8b21489e6538d15ca74bc3fff00fc309b949ed93770ba5249`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.0 KB (5036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cc9f66c99b70c75f3c3a9e5d7fcf285ae5328205a9aea24fec87135908f3a7`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.37`

```console
$ docker pull mariadb@sha256:8a438741fde0e57870131c7641aa9fd806157bde3971768daa10779c21a9ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.37` - linux; amd64

```console
$ docker pull mariadb@sha256:439b0f747583815a1b19bf6bbb021f572d512b5e7b7f8ead02efa6f56ca2709b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107994969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ea9f3c9867ea2da7cef023c8c2635fd5307c8aa494870c2ab9770f171143c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 04:31:46 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:32:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:32:18 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:32:18 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:32:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:32:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:32:19 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f2d0ff8f45d43dffd1135bda5a1dc7105de6ddf9bf9a9ed5e4bddb84f137f`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ca81f3f39b625e126d993555a098320bbae31fe0b4ff49ee83663d35662ff`  
		Last Modified: Thu, 04 Mar 2021 04:34:51 GMT  
		Size: 74.2 MB (74196878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee9bfeecca0b294ed9602c569c4fbc00c83187f8fe7c918a9fc0bf0b54ac025`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54099fae91675f0a37ebbd7b729d527fdbf8f0726c7850b50b78eef1fb777fbc`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.37` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:41e0b44b138e68dff225a31d162581175d4a900753dd6ec0ca3d175e156b23f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103141928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e10db427fd771b9c53b44b2b080f88ab5fb0ef3db5afff19bf1e338c8f80f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:11:07 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 05:11:08 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 05:11:10 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:11:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:11:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:11:52 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:11:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:11:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:11:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59d5168fcca261f6c64f3e7c589f45639812c32e8faad9e393c2d9d5eee3ebd`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47601255f2573ec41073df7102597f8ebb232d95034e9cc508fe57cbb529cf41`  
		Last Modified: Thu, 04 Mar 2021 05:15:49 GMT  
		Size: 72.8 MB (72811904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e95411cf8aad99aa40fbbfffea2ab171af3290807f90265f377ba1b6daad4`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e241069f86657853a4833dd08af7b6d75d5e8aaa8e1af424246d0ee08fcbc`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.37` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6f9c8f2dba5b006608bd11c44a7dc321c98028c731a4a09eb1938053ce103719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca52c5eab0773f9a18fa387b3573b90662f2498d00a7afd1a115699e0d4e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:41:58 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 06:42:07 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 06:42:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:46:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:46:17 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:46:19 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:46:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:46:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:46:45 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:46:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997301be2225c5dd5af97c84c36ea5eeb7b94dad8578e61b792a791538d8ed5d`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfa86a6fdedeff2832388e3cba3b6c711584f861e46280359018eacc99c407a`  
		Last Modified: Thu, 04 Mar 2021 06:56:46 GMT  
		Size: 77.8 MB (77768320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab67bd3f9ac2a8b21489e6538d15ca74bc3fff00fc309b949ed93770ba5249`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.0 KB (5036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cc9f66c99b70c75f3c3a9e5d7fcf285ae5328205a9aea24fec87135908f3a7`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.37-bionic`

```console
$ docker pull mariadb@sha256:8a438741fde0e57870131c7641aa9fd806157bde3971768daa10779c21a9ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.37-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:439b0f747583815a1b19bf6bbb021f572d512b5e7b7f8ead02efa6f56ca2709b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107994969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ea9f3c9867ea2da7cef023c8c2635fd5307c8aa494870c2ab9770f171143c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 04:31:46 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:32:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:32:18 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:32:18 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:32:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:32:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:32:19 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f2d0ff8f45d43dffd1135bda5a1dc7105de6ddf9bf9a9ed5e4bddb84f137f`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ca81f3f39b625e126d993555a098320bbae31fe0b4ff49ee83663d35662ff`  
		Last Modified: Thu, 04 Mar 2021 04:34:51 GMT  
		Size: 74.2 MB (74196878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee9bfeecca0b294ed9602c569c4fbc00c83187f8fe7c918a9fc0bf0b54ac025`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54099fae91675f0a37ebbd7b729d527fdbf8f0726c7850b50b78eef1fb777fbc`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.37-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:41e0b44b138e68dff225a31d162581175d4a900753dd6ec0ca3d175e156b23f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103141928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e10db427fd771b9c53b44b2b080f88ab5fb0ef3db5afff19bf1e338c8f80f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:11:07 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 05:11:08 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 05:11:10 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:11:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:11:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:11:52 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:11:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:11:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:11:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59d5168fcca261f6c64f3e7c589f45639812c32e8faad9e393c2d9d5eee3ebd`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47601255f2573ec41073df7102597f8ebb232d95034e9cc508fe57cbb529cf41`  
		Last Modified: Thu, 04 Mar 2021 05:15:49 GMT  
		Size: 72.8 MB (72811904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e95411cf8aad99aa40fbbfffea2ab171af3290807f90265f377ba1b6daad4`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e241069f86657853a4833dd08af7b6d75d5e8aaa8e1af424246d0ee08fcbc`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.37-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6f9c8f2dba5b006608bd11c44a7dc321c98028c731a4a09eb1938053ce103719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca52c5eab0773f9a18fa387b3573b90662f2498d00a7afd1a115699e0d4e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:41:58 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 06:42:07 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 06:42:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:46:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:46:17 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:46:19 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:46:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:46:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:46:45 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:46:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997301be2225c5dd5af97c84c36ea5eeb7b94dad8578e61b792a791538d8ed5d`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfa86a6fdedeff2832388e3cba3b6c711584f861e46280359018eacc99c407a`  
		Last Modified: Thu, 04 Mar 2021 06:56:46 GMT  
		Size: 77.8 MB (77768320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab67bd3f9ac2a8b21489e6538d15ca74bc3fff00fc309b949ed93770ba5249`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.0 KB (5036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cc9f66c99b70c75f3c3a9e5d7fcf285ae5328205a9aea24fec87135908f3a7`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:8a438741fde0e57870131c7641aa9fd806157bde3971768daa10779c21a9ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:439b0f747583815a1b19bf6bbb021f572d512b5e7b7f8ead02efa6f56ca2709b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107994969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ea9f3c9867ea2da7cef023c8c2635fd5307c8aa494870c2ab9770f171143c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:31:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:31:25 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:25 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:31:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:31:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:31:43 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:31:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 04:31:45 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 04:31:46 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:32:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:32:18 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:32:18 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:32:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:32:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:32:19 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae230813b90234b65b732e242b58bdfb7b6f0692ae242e9265b89a29672c3f0`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4f01551c9be291f03a416b6703e692962f17e1077ea999d94f54d518c06623`  
		Last Modified: Thu, 04 Mar 2021 04:34:40 GMT  
		Size: 4.8 MB (4812925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19708427784f8f870301f1fc9207ae3fe39fa2df4030fd911f73dfae5e9daa29`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 1.3 MB (1327807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782e8cbdb8eae3356c4e74b41ce130f455a4a26cb0bc52c2f6334cddc83aba8`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780475c233af1c7e8e544db27f07b8b692be8e2170345ec854283a8af35264a9`  
		Last Modified: Thu, 04 Mar 2021 04:34:39 GMT  
		Size: 933.6 KB (933554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955196b1da1a74e1cdbadc8350be6ed904b791288b7a98f96dedf52a9284c172`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f2d0ff8f45d43dffd1135bda5a1dc7105de6ddf9bf9a9ed5e4bddb84f137f`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ca81f3f39b625e126d993555a098320bbae31fe0b4ff49ee83663d35662ff`  
		Last Modified: Thu, 04 Mar 2021 04:34:51 GMT  
		Size: 74.2 MB (74196878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee9bfeecca0b294ed9602c569c4fbc00c83187f8fe7c918a9fc0bf0b54ac025`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54099fae91675f0a37ebbd7b729d527fdbf8f0726c7850b50b78eef1fb777fbc`  
		Last Modified: Thu, 04 Mar 2021 04:34:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:41e0b44b138e68dff225a31d162581175d4a900753dd6ec0ca3d175e156b23f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103141928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e10db427fd771b9c53b44b2b080f88ab5fb0ef3db5afff19bf1e338c8f80f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:10:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:10:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:10:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:10:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:11:04 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:11:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:11:07 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 05:11:08 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 05:11:10 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:11:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:11:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:11:52 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:11:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:11:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:11:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:11:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e768d1abdfd87df0349ec468eed8204dd8dae6381830359580e475c44664072b`  
		Last Modified: Thu, 04 Mar 2021 05:15:34 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd311d50ef9df42e553d51895015673476349bb8fda3c675bb7b1a0559a591f4`  
		Last Modified: Thu, 04 Mar 2021 05:15:35 GMT  
		Size: 4.4 MB (4395344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1378964f992f70ea2aeba0f2e95385d3ce16074e15d2ad00875d5602047a340`  
		Last Modified: Thu, 04 Mar 2021 05:15:33 GMT  
		Size: 1.3 MB (1263677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d5def3a3efceac6bde44d34990b06ed76fbdaa7b7d5331d270655778fb91`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9daf6c866e4bffe5d598f4874bdf5a8c092981b26c40051deccaa1cc3ec07e`  
		Last Modified: Thu, 04 Mar 2021 05:15:32 GMT  
		Size: 925.2 KB (925219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160da646e578263bf16e369d8780f1faa61b970dea2cccf4e559e57238c20b6d`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59d5168fcca261f6c64f3e7c589f45639812c32e8faad9e393c2d9d5eee3ebd`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47601255f2573ec41073df7102597f8ebb232d95034e9cc508fe57cbb529cf41`  
		Last Modified: Thu, 04 Mar 2021 05:15:49 GMT  
		Size: 72.8 MB (72811904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e95411cf8aad99aa40fbbfffea2ab171af3290807f90265f377ba1b6daad4`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e241069f86657853a4833dd08af7b6d75d5e8aaa8e1af424246d0ee08fcbc`  
		Last Modified: Thu, 04 Mar 2021 05:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6f9c8f2dba5b006608bd11c44a7dc321c98028c731a4a09eb1938053ce103719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca52c5eab0773f9a18fa387b3573b90662f2498d00a7afd1a115699e0d4e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:56:30 GMT
ADD file:4a2d847969faa9da1f1336ff0c2871a418cb7f7668abecb0d6914821ce7acd02 in / 
# Thu, 04 Mar 2021 02:56:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:57:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:57:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:57:22 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:37:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:39:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:39:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:40:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:41:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:41:35 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:41:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:41:58 GMT
ENV MARIADB_MAJOR=10.2
# Thu, 04 Mar 2021 06:42:07 GMT
ENV MARIADB_VERSION=1:10.2.37+maria~bionic
# Thu, 04 Mar 2021 06:42:26 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:46:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:46:17 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:46:19 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:46:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:46:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:46:45 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:46:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:367a668e4ea4eecc7411f59b0e710bd8e6f0910afffbc5cf7cc56a9b91cf2097`  
		Last Modified: Mon, 01 Mar 2021 16:20:21 GMT  
		Size: 30.4 MB (30421101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1a50fb15144b9c99d82c9511112522bcbc25c056716cb225e51c2998a3c4c5`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d4006473f93104f15e85c85416b0e4a37cb8c0f58552fc6f9260fe2c58140`  
		Last Modified: Thu, 04 Mar 2021 03:01:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6b37af157aea7b03bdd2bf7eb6782c48c96c0d8a6eef9887ba644b84153926`  
		Last Modified: Thu, 04 Mar 2021 06:56:36 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2086ba108d057cb425100f75abd71bc7179a568c13f4c240ac82cea9d6cf269b`  
		Last Modified: Thu, 04 Mar 2021 06:56:35 GMT  
		Size: 5.6 MB (5630295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf845d66a4c46d76b1df958f50c663a1550a1790c30de034e7f1917fd1aae44e`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 1.2 MB (1246995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a6fbf1d3f16f5f970530dece2d9bca2c4e8348d4c47b24b44ada79b1989250`  
		Last Modified: Thu, 04 Mar 2021 06:56:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974a98ab929d3c77e0cbb8f9993260df628738759b920e8194e14d831ca47fb`  
		Last Modified: Thu, 04 Mar 2021 06:56:33 GMT  
		Size: 934.9 KB (934883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519f971c7bd635ebc9f54741fb92ecaba23484d181a09d29389db328a81b0359`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997301be2225c5dd5af97c84c36ea5eeb7b94dad8578e61b792a791538d8ed5d`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfa86a6fdedeff2832388e3cba3b6c711584f861e46280359018eacc99c407a`  
		Last Modified: Thu, 04 Mar 2021 06:56:46 GMT  
		Size: 77.8 MB (77768320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab67bd3f9ac2a8b21489e6538d15ca74bc3fff00fc309b949ed93770ba5249`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 5.0 KB (5036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cc9f66c99b70c75f3c3a9e5d7fcf285ae5328205a9aea24fec87135908f3a7`  
		Last Modified: Thu, 04 Mar 2021 06:56:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:518be0d8a58b0f080eb623549c6a58bcad3e4a4489af447a0c612067ed474ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:2d68fb61b0924371cae8c59f33826c4f9933602280598edac67ab8b62c62ea86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118347191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974ca79075643f6080d25d82fcf6f346b8050af60b6e1d2419db31ade3bf57b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 04:30:42 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:31:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:31:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:31:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:31:09 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:31:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f532cb204a7181f6ff531a4232b09f360ef4e6c102a80d04926b3d7a209e21`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122708f0357f77a078f63eb5b04790c7f5197e744c8795360f4497b388c0425`  
		Last Modified: Thu, 04 Mar 2021 04:34:32 GMT  
		Size: 81.7 MB (81682193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6259f0b4b4758dd1b6d75410bab7ad22e7e0696ed76085504a76e10fadb62`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed977c5a658232212863707c5a32e570a08f155ee2ab5d86b074bdd12075e7d`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d636eb716f494af3224d2b718248f9d55904564f3e8f41b1df90ed0d0f3fa870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116035774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dc2a485c3750edd5c3168876541719522637c3fbedb30af07efeb15d7262ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 05:09:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:09:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:09:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:09:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:09:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:09:58 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:09:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c12284efd58aeff0ba4bdd1637a784186a1bb6173eb7e859852461a73f5e9`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c8be748ee8736e21c65267a5d20f5b98f5e092ced9b88e056108a692a049b`  
		Last Modified: Thu, 04 Mar 2021 05:15:21 GMT  
		Size: 80.9 MB (80861401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d4b81455a66dc3ca164bd0b6d2c7f9896af34fa0a162f60e1a0eb4704774b`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805638aa8a32062123881f10f2efd14ed80e47ceebf33077e0ba21522030e93c`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c75820bf24d33ff849b07b4b94653b260f39f660bd71b964f4036b211e417823
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128921536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655d729966bbe6d60a9fc49d932f801ae769f09c98cd0265c11b23569aee05d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:31:39 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 06:31:42 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 06:31:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:35:44 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:35:59 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:36:03 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:36:29 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:36:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec31dae91eee2c8e538dbefd25fbf2bf909fb84b310f0cad5a1212927944030`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1033f8cb1b2569e9295248a52a307772a3a3ddd68851f4289f25cb62cbe0385d`  
		Last Modified: Thu, 04 Mar 2021 06:56:06 GMT  
		Size: 86.4 MB (86437200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c524a087892c4c46b8083439ff6a2f45db62970db5686bf369e69cc3f2210d21`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90f436da1382f3de30c9bbfe60762627a3378ef3c5b84a31044997a3f046f45`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.28`

```console
$ docker pull mariadb@sha256:518be0d8a58b0f080eb623549c6a58bcad3e4a4489af447a0c612067ed474ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.28` - linux; amd64

```console
$ docker pull mariadb@sha256:2d68fb61b0924371cae8c59f33826c4f9933602280598edac67ab8b62c62ea86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118347191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974ca79075643f6080d25d82fcf6f346b8050af60b6e1d2419db31ade3bf57b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 04:30:42 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:31:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:31:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:31:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:31:09 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:31:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f532cb204a7181f6ff531a4232b09f360ef4e6c102a80d04926b3d7a209e21`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122708f0357f77a078f63eb5b04790c7f5197e744c8795360f4497b388c0425`  
		Last Modified: Thu, 04 Mar 2021 04:34:32 GMT  
		Size: 81.7 MB (81682193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6259f0b4b4758dd1b6d75410bab7ad22e7e0696ed76085504a76e10fadb62`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed977c5a658232212863707c5a32e570a08f155ee2ab5d86b074bdd12075e7d`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.28` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d636eb716f494af3224d2b718248f9d55904564f3e8f41b1df90ed0d0f3fa870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116035774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dc2a485c3750edd5c3168876541719522637c3fbedb30af07efeb15d7262ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 05:09:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:09:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:09:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:09:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:09:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:09:58 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:09:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c12284efd58aeff0ba4bdd1637a784186a1bb6173eb7e859852461a73f5e9`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c8be748ee8736e21c65267a5d20f5b98f5e092ced9b88e056108a692a049b`  
		Last Modified: Thu, 04 Mar 2021 05:15:21 GMT  
		Size: 80.9 MB (80861401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d4b81455a66dc3ca164bd0b6d2c7f9896af34fa0a162f60e1a0eb4704774b`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805638aa8a32062123881f10f2efd14ed80e47ceebf33077e0ba21522030e93c`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.28` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c75820bf24d33ff849b07b4b94653b260f39f660bd71b964f4036b211e417823
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128921536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655d729966bbe6d60a9fc49d932f801ae769f09c98cd0265c11b23569aee05d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:31:39 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 06:31:42 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 06:31:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:35:44 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:35:59 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:36:03 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:36:29 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:36:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec31dae91eee2c8e538dbefd25fbf2bf909fb84b310f0cad5a1212927944030`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1033f8cb1b2569e9295248a52a307772a3a3ddd68851f4289f25cb62cbe0385d`  
		Last Modified: Thu, 04 Mar 2021 06:56:06 GMT  
		Size: 86.4 MB (86437200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c524a087892c4c46b8083439ff6a2f45db62970db5686bf369e69cc3f2210d21`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90f436da1382f3de30c9bbfe60762627a3378ef3c5b84a31044997a3f046f45`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.28-focal`

```console
$ docker pull mariadb@sha256:518be0d8a58b0f080eb623549c6a58bcad3e4a4489af447a0c612067ed474ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.28-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2d68fb61b0924371cae8c59f33826c4f9933602280598edac67ab8b62c62ea86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118347191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974ca79075643f6080d25d82fcf6f346b8050af60b6e1d2419db31ade3bf57b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 04:30:42 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:31:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:31:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:31:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:31:09 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:31:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f532cb204a7181f6ff531a4232b09f360ef4e6c102a80d04926b3d7a209e21`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122708f0357f77a078f63eb5b04790c7f5197e744c8795360f4497b388c0425`  
		Last Modified: Thu, 04 Mar 2021 04:34:32 GMT  
		Size: 81.7 MB (81682193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6259f0b4b4758dd1b6d75410bab7ad22e7e0696ed76085504a76e10fadb62`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed977c5a658232212863707c5a32e570a08f155ee2ab5d86b074bdd12075e7d`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.28-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d636eb716f494af3224d2b718248f9d55904564f3e8f41b1df90ed0d0f3fa870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116035774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dc2a485c3750edd5c3168876541719522637c3fbedb30af07efeb15d7262ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 05:09:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:09:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:09:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:09:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:09:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:09:58 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:09:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c12284efd58aeff0ba4bdd1637a784186a1bb6173eb7e859852461a73f5e9`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c8be748ee8736e21c65267a5d20f5b98f5e092ced9b88e056108a692a049b`  
		Last Modified: Thu, 04 Mar 2021 05:15:21 GMT  
		Size: 80.9 MB (80861401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d4b81455a66dc3ca164bd0b6d2c7f9896af34fa0a162f60e1a0eb4704774b`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805638aa8a32062123881f10f2efd14ed80e47ceebf33077e0ba21522030e93c`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.28-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c75820bf24d33ff849b07b4b94653b260f39f660bd71b964f4036b211e417823
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128921536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655d729966bbe6d60a9fc49d932f801ae769f09c98cd0265c11b23569aee05d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:31:39 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 06:31:42 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 06:31:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:35:44 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:35:59 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:36:03 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:36:29 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:36:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec31dae91eee2c8e538dbefd25fbf2bf909fb84b310f0cad5a1212927944030`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1033f8cb1b2569e9295248a52a307772a3a3ddd68851f4289f25cb62cbe0385d`  
		Last Modified: Thu, 04 Mar 2021 06:56:06 GMT  
		Size: 86.4 MB (86437200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c524a087892c4c46b8083439ff6a2f45db62970db5686bf369e69cc3f2210d21`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90f436da1382f3de30c9bbfe60762627a3378ef3c5b84a31044997a3f046f45`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:518be0d8a58b0f080eb623549c6a58bcad3e4a4489af447a0c612067ed474ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2d68fb61b0924371cae8c59f33826c4f9933602280598edac67ab8b62c62ea86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118347191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974ca79075643f6080d25d82fcf6f346b8050af60b6e1d2419db31ade3bf57b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 04:30:41 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 04:30:42 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:31:07 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:31:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:31:08 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:31:09 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:31:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f532cb204a7181f6ff531a4232b09f360ef4e6c102a80d04926b3d7a209e21`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122708f0357f77a078f63eb5b04790c7f5197e744c8795360f4497b388c0425`  
		Last Modified: Thu, 04 Mar 2021 04:34:32 GMT  
		Size: 81.7 MB (81682193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6259f0b4b4758dd1b6d75410bab7ad22e7e0696ed76085504a76e10fadb62`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed977c5a658232212863707c5a32e570a08f155ee2ab5d86b074bdd12075e7d`  
		Last Modified: Thu, 04 Mar 2021 04:34:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d636eb716f494af3224d2b718248f9d55904564f3e8f41b1df90ed0d0f3fa870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116035774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dc2a485c3750edd5c3168876541719522637c3fbedb30af07efeb15d7262ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 05:09:04 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 05:09:06 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:09:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:09:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:09:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:09:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:09:58 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:09:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c12284efd58aeff0ba4bdd1637a784186a1bb6173eb7e859852461a73f5e9`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c8be748ee8736e21c65267a5d20f5b98f5e092ced9b88e056108a692a049b`  
		Last Modified: Thu, 04 Mar 2021 05:15:21 GMT  
		Size: 80.9 MB (80861401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d4b81455a66dc3ca164bd0b6d2c7f9896af34fa0a162f60e1a0eb4704774b`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805638aa8a32062123881f10f2efd14ed80e47ceebf33077e0ba21522030e93c`  
		Last Modified: Thu, 04 Mar 2021 05:14:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c75820bf24d33ff849b07b4b94653b260f39f660bd71b964f4036b211e417823
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128921536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655d729966bbe6d60a9fc49d932f801ae769f09c98cd0265c11b23569aee05d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:31:39 GMT
ENV MARIADB_MAJOR=10.3
# Thu, 04 Mar 2021 06:31:42 GMT
ENV MARIADB_VERSION=1:10.3.28+maria~focal
# Thu, 04 Mar 2021 06:31:56 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:35:44 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:35:59 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:36:03 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:36:29 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:36:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec31dae91eee2c8e538dbefd25fbf2bf909fb84b310f0cad5a1212927944030`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1033f8cb1b2569e9295248a52a307772a3a3ddd68851f4289f25cb62cbe0385d`  
		Last Modified: Thu, 04 Mar 2021 06:56:06 GMT  
		Size: 86.4 MB (86437200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c524a087892c4c46b8083439ff6a2f45db62970db5686bf369e69cc3f2210d21`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 5.0 KB (5032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90f436da1382f3de30c9bbfe60762627a3378ef3c5b84a31044997a3f046f45`  
		Last Modified: Thu, 04 Mar 2021 06:55:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:2989c7dd00995a73e858f647f3603a9932546f5792d1934127d66f1cf762205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:098651cb7ac514642dde2c85eeb438a33a0963a907cb9cea497ab8c43a15c7e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122223944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30b8e81d0ebca7e8a6bf7b8640ef3aa8d81970047a4ed6a2a806ffdbe72bb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 04:30:07 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:30:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:30:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:30:30 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:30:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:30:32 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:30:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea6f849a3c53ee04c470fc6953c7e846eda854923c359cde07a8273d879540`  
		Last Modified: Thu, 04 Mar 2021 04:33:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ebd461509178cb969fed10514a607955276840b82f965824af053b9726e4`  
		Last Modified: Thu, 04 Mar 2021 04:34:11 GMT  
		Size: 85.6 MB (85558945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421444cebf598a0c91bdd16ae543624b2ecc47c8de2ab9748dbd67f31b63bdad`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282b3e8846b8017fd6d7ef0f8ece70d108567d2c44d104a6d1245c156e7026a`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:30474baa22e0dd6ab015574d76cbbb6c744786670e7d1a843768dcf6c7b33154
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119804800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeacf3267ff3af94a6b8e9621f84408db169cebf1fde7932e2f66fccad619244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:08:13 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 05:08:14 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 05:08:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:08:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:08:52 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:08:53 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:08:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:08:56 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:08:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbe11de7008cafa27dc1f3097d6a33e941ece4feae2b9803b36885f5247ccfe`  
		Last Modified: Thu, 04 Mar 2021 05:14:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2f14d27886168154850ef4e027de00de30e4817d7e3b2506b2c537bfd6616a`  
		Last Modified: Thu, 04 Mar 2021 05:14:47 GMT  
		Size: 84.6 MB (84630428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6247566095fa172218d61592e09bbe6dbd4bfea2a58230f9ef0b7ca9da35e352`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a62f433076ae5ecd9904a90ebcefa2e05fdbc79e80abba79381a7704b4d4d9`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1a6a6208cda5911680e18201ed91ac8bea459a2eee830cdb60d229391f2f35e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132600360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa0c1a1a1a4a31d99f99cdbd9a0c329eb17af597678fbca5e30c217e26a7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:24:10 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 06:24:13 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 06:24:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:30:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:30:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:30:48 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:31:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:31:16 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:31:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c205ece48ede7e88894837d8681c3a1ea49761346c1e8bc5348eea510bec15a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66e0781b08a9686d8e20bcb506e57616ff3f656c5c16617a89826442a049aa`  
		Last Modified: Thu, 04 Mar 2021 06:55:28 GMT  
		Size: 90.1 MB (90116018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5420aa9c073b603c6139583454d35dafe0ec69eb261ab13623d8b8a25bc1a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c6789ba95d918d2d38729d9ef2197e69bdab546f91818d87bad0b7dc7eecb`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.18`

```console
$ docker pull mariadb@sha256:2989c7dd00995a73e858f647f3603a9932546f5792d1934127d66f1cf762205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.18` - linux; amd64

```console
$ docker pull mariadb@sha256:098651cb7ac514642dde2c85eeb438a33a0963a907cb9cea497ab8c43a15c7e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122223944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30b8e81d0ebca7e8a6bf7b8640ef3aa8d81970047a4ed6a2a806ffdbe72bb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 04:30:07 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:30:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:30:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:30:30 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:30:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:30:32 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:30:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea6f849a3c53ee04c470fc6953c7e846eda854923c359cde07a8273d879540`  
		Last Modified: Thu, 04 Mar 2021 04:33:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ebd461509178cb969fed10514a607955276840b82f965824af053b9726e4`  
		Last Modified: Thu, 04 Mar 2021 04:34:11 GMT  
		Size: 85.6 MB (85558945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421444cebf598a0c91bdd16ae543624b2ecc47c8de2ab9748dbd67f31b63bdad`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282b3e8846b8017fd6d7ef0f8ece70d108567d2c44d104a6d1245c156e7026a`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.18` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:30474baa22e0dd6ab015574d76cbbb6c744786670e7d1a843768dcf6c7b33154
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119804800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeacf3267ff3af94a6b8e9621f84408db169cebf1fde7932e2f66fccad619244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:08:13 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 05:08:14 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 05:08:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:08:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:08:52 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:08:53 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:08:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:08:56 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:08:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbe11de7008cafa27dc1f3097d6a33e941ece4feae2b9803b36885f5247ccfe`  
		Last Modified: Thu, 04 Mar 2021 05:14:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2f14d27886168154850ef4e027de00de30e4817d7e3b2506b2c537bfd6616a`  
		Last Modified: Thu, 04 Mar 2021 05:14:47 GMT  
		Size: 84.6 MB (84630428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6247566095fa172218d61592e09bbe6dbd4bfea2a58230f9ef0b7ca9da35e352`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a62f433076ae5ecd9904a90ebcefa2e05fdbc79e80abba79381a7704b4d4d9`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.18` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1a6a6208cda5911680e18201ed91ac8bea459a2eee830cdb60d229391f2f35e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132600360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa0c1a1a1a4a31d99f99cdbd9a0c329eb17af597678fbca5e30c217e26a7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:24:10 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 06:24:13 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 06:24:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:30:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:30:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:30:48 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:31:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:31:16 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:31:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c205ece48ede7e88894837d8681c3a1ea49761346c1e8bc5348eea510bec15a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66e0781b08a9686d8e20bcb506e57616ff3f656c5c16617a89826442a049aa`  
		Last Modified: Thu, 04 Mar 2021 06:55:28 GMT  
		Size: 90.1 MB (90116018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5420aa9c073b603c6139583454d35dafe0ec69eb261ab13623d8b8a25bc1a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c6789ba95d918d2d38729d9ef2197e69bdab546f91818d87bad0b7dc7eecb`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.18-focal`

```console
$ docker pull mariadb@sha256:2989c7dd00995a73e858f647f3603a9932546f5792d1934127d66f1cf762205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.18-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:098651cb7ac514642dde2c85eeb438a33a0963a907cb9cea497ab8c43a15c7e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122223944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30b8e81d0ebca7e8a6bf7b8640ef3aa8d81970047a4ed6a2a806ffdbe72bb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 04:30:07 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:30:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:30:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:30:30 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:30:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:30:32 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:30:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea6f849a3c53ee04c470fc6953c7e846eda854923c359cde07a8273d879540`  
		Last Modified: Thu, 04 Mar 2021 04:33:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ebd461509178cb969fed10514a607955276840b82f965824af053b9726e4`  
		Last Modified: Thu, 04 Mar 2021 04:34:11 GMT  
		Size: 85.6 MB (85558945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421444cebf598a0c91bdd16ae543624b2ecc47c8de2ab9748dbd67f31b63bdad`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282b3e8846b8017fd6d7ef0f8ece70d108567d2c44d104a6d1245c156e7026a`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.18-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:30474baa22e0dd6ab015574d76cbbb6c744786670e7d1a843768dcf6c7b33154
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119804800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeacf3267ff3af94a6b8e9621f84408db169cebf1fde7932e2f66fccad619244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:08:13 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 05:08:14 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 05:08:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:08:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:08:52 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:08:53 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:08:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:08:56 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:08:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbe11de7008cafa27dc1f3097d6a33e941ece4feae2b9803b36885f5247ccfe`  
		Last Modified: Thu, 04 Mar 2021 05:14:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2f14d27886168154850ef4e027de00de30e4817d7e3b2506b2c537bfd6616a`  
		Last Modified: Thu, 04 Mar 2021 05:14:47 GMT  
		Size: 84.6 MB (84630428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6247566095fa172218d61592e09bbe6dbd4bfea2a58230f9ef0b7ca9da35e352`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a62f433076ae5ecd9904a90ebcefa2e05fdbc79e80abba79381a7704b4d4d9`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.18-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1a6a6208cda5911680e18201ed91ac8bea459a2eee830cdb60d229391f2f35e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132600360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa0c1a1a1a4a31d99f99cdbd9a0c329eb17af597678fbca5e30c217e26a7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:24:10 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 06:24:13 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 06:24:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:30:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:30:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:30:48 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:31:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:31:16 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:31:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c205ece48ede7e88894837d8681c3a1ea49761346c1e8bc5348eea510bec15a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66e0781b08a9686d8e20bcb506e57616ff3f656c5c16617a89826442a049aa`  
		Last Modified: Thu, 04 Mar 2021 06:55:28 GMT  
		Size: 90.1 MB (90116018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5420aa9c073b603c6139583454d35dafe0ec69eb261ab13623d8b8a25bc1a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c6789ba95d918d2d38729d9ef2197e69bdab546f91818d87bad0b7dc7eecb`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:2989c7dd00995a73e858f647f3603a9932546f5792d1934127d66f1cf762205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:098651cb7ac514642dde2c85eeb438a33a0963a907cb9cea497ab8c43a15c7e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122223944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30b8e81d0ebca7e8a6bf7b8640ef3aa8d81970047a4ed6a2a806ffdbe72bb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 04:30:06 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 04:30:07 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:30:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:30:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:30:30 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:30:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 04:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:30:32 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:30:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea6f849a3c53ee04c470fc6953c7e846eda854923c359cde07a8273d879540`  
		Last Modified: Thu, 04 Mar 2021 04:33:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ebd461509178cb969fed10514a607955276840b82f965824af053b9726e4`  
		Last Modified: Thu, 04 Mar 2021 04:34:11 GMT  
		Size: 85.6 MB (85558945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421444cebf598a0c91bdd16ae543624b2ecc47c8de2ab9748dbd67f31b63bdad`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282b3e8846b8017fd6d7ef0f8ece70d108567d2c44d104a6d1245c156e7026a`  
		Last Modified: Thu, 04 Mar 2021 04:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:30474baa22e0dd6ab015574d76cbbb6c744786670e7d1a843768dcf6c7b33154
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119804800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeacf3267ff3af94a6b8e9621f84408db169cebf1fde7932e2f66fccad619244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:08:13 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 05:08:14 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 05:08:16 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:08:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:08:52 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:08:53 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:08:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 05:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:08:56 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:08:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbe11de7008cafa27dc1f3097d6a33e941ece4feae2b9803b36885f5247ccfe`  
		Last Modified: Thu, 04 Mar 2021 05:14:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2f14d27886168154850ef4e027de00de30e4817d7e3b2506b2c537bfd6616a`  
		Last Modified: Thu, 04 Mar 2021 05:14:47 GMT  
		Size: 84.6 MB (84630428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6247566095fa172218d61592e09bbe6dbd4bfea2a58230f9ef0b7ca9da35e352`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 5.0 KB (5031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a62f433076ae5ecd9904a90ebcefa2e05fdbc79e80abba79381a7704b4d4d9`  
		Last Modified: Thu, 04 Mar 2021 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1a6a6208cda5911680e18201ed91ac8bea459a2eee830cdb60d229391f2f35e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132600360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa0c1a1a1a4a31d99f99cdbd9a0c329eb17af597678fbca5e30c217e26a7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:24:10 GMT
ENV MARIADB_MAJOR=10.4
# Thu, 04 Mar 2021 06:24:13 GMT
ENV MARIADB_VERSION=1:10.4.18+maria~focal
# Thu, 04 Mar 2021 06:24:25 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:30:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:30:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:30:48 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:31:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 06:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:31:16 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:31:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c205ece48ede7e88894837d8681c3a1ea49761346c1e8bc5348eea510bec15a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66e0781b08a9686d8e20bcb506e57616ff3f656c5c16617a89826442a049aa`  
		Last Modified: Thu, 04 Mar 2021 06:55:28 GMT  
		Size: 90.1 MB (90116018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5420aa9c073b603c6139583454d35dafe0ec69eb261ab13623d8b8a25bc1a`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 5.0 KB (5035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c6789ba95d918d2d38729d9ef2197e69bdab546f91818d87bad0b7dc7eecb`  
		Last Modified: Thu, 04 Mar 2021 06:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.9`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.9` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.9-focal`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.9-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.9-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.9-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:54b817feea3022688e49aeb70b27d4cc6aa08de0b114bd664b9194b549a1d277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:66904d015f15ee476bf4523812aaf2ee6057f9fc8a9615e7c559345bd3a7ce77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124238585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27cf5bc24fe85c16570e03c560dfd28661d7ae9aa568603b16b51f7013ba44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 04:29:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:10 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 04:29:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 04:29:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 04:29:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:29:26 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 04:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 04:29:27 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 04:29:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 04:29:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 04:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 04:29:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 04:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 04:29:55 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 04:29:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2722e0986c49e3377e1adee02b9422ce5a86b79d2124417a401f08c3a2ef`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d25563a9faa3defd0a1f3d86e8d4d1cfdc4e137c6623e1a9a0c8be6d74037`  
		Last Modified: Thu, 04 Mar 2021 04:33:34 GMT  
		Size: 5.5 MB (5488607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022ea4dab7700ee26594423c28da944c8c39b5ddefc168e0d347cc3b80c0624`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 1.3 MB (1325505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab4098b0f7c256fa8af78f8cd8841e3a3e92302920bfb148f078035ddc9b33c`  
		Last Modified: Thu, 04 Mar 2021 04:33:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03413915fdf2f0090634cde87bec1937d70bb5eb2c3e624413bfe74f5d6d02b`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 1.3 MB (1272252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8e671b1408d47d9639e53a73240074ca70922aa4bc5bfca75d56a4f37e3084`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2452f3fb5ccd207ff43095fe46ff34ef4c1718ee16eb595032c7b97cf5d722`  
		Last Modified: Thu, 04 Mar 2021 04:33:32 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2da3a6fe532488b5943ba52b8fe05d5399b179e6bbc7bbe0d787fd4630a67d8`  
		Last Modified: Thu, 04 Mar 2021 04:33:47 GMT  
		Size: 87.6 MB (87573707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b7df268e7bed86bbaa23d388d1fcb121a1ef1ef37e5af0baf8c946f454577`  
		Last Modified: Thu, 04 Mar 2021 04:33:31 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5af12825042cf1d9cc510e9f2b6417bbce30a01e888e53249d8c0246c2fb939a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121826466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939d05495a900b17e3000050111db49d7439a004cdd0e2d1cb17a80527231cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 05:06:26 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 05:06:43 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:06:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 05:06:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 05:07:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 05:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:07:13 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 05:07:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 05:07:16 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 05:07:18 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 05:07:52 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 05:07:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 05:07:55 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 05:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 05:07:57 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 05:07:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b95d441842412b8c4ba98c3a4ed7999f33e6b3a74e0bb1e15af85fa8c30b3`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a02ed92077601d993fb3fe8bd61397b24037ae5ba38c58e7a013f291b5821c`  
		Last Modified: Thu, 04 Mar 2021 05:13:46 GMT  
		Size: 5.5 MB (5455153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea02edf9bf7ccc95d89d450509cbfe315e94cde48b441eaef870143b149e4cd`  
		Last Modified: Thu, 04 Mar 2021 05:13:45 GMT  
		Size: 1.3 MB (1261790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24c9bd9fe3a3f0f5a0a1ac338341775cbbd3033a0137f2f7067e62a8a40273`  
		Last Modified: Thu, 04 Mar 2021 05:13:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d5537d6c906af49a86cefa3ee693cc2b194f451c8b2888f78cb9f2622ee9f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 1.3 MB (1270716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e2f0e8909b5436b7975a5866f9d155da9a84e4ad9ba4f0e4b107f6970b09f`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414d2a5d07d6248cc0d25463e4a918acbb9affea4a85d702835a5275e565456`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f2315346cb9617481664f3de9f363f8850f298a1d757a4ca5b0e076bb34f9`  
		Last Modified: Thu, 04 Mar 2021 05:14:05 GMT  
		Size: 86.7 MB (86652213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbfe2815f55f6e246578c644c8b94f23f2b5be6aae2c66b995c487f9032bf93`  
		Last Modified: Thu, 04 Mar 2021 05:13:43 GMT  
		Size: 5.0 KB (5034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e44223a51ea890f8c371bc6762ed0e82538a95d8617d76f5660741de3385b17f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99835644e8056755786580ea0a06ce97a8a7970c172013c310c588803c6b4ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Mar 2021 02:57:39 GMT
ADD file:b709cd21d0acd910f23e8ad46933746a841aeac2e6e28c7c42fe92616cdbfa0d in / 
# Thu, 04 Mar 2021 02:58:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:58:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:58:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:58:46 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 06:14:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 04 Mar 2021 06:16:36 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:16:44 GMT
ENV GOSU_VERSION=1.12
# Thu, 04 Mar 2021 06:18:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Mar 2021 06:18:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 Mar 2021 06:19:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 06:19:16 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 04 Mar 2021 06:19:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 04 Mar 2021 06:19:48 GMT
ENV MARIADB_MAJOR=10.5
# Thu, 04 Mar 2021 06:19:52 GMT
ENV MARIADB_VERSION=1:10.5.9+maria~focal
# Thu, 04 Mar 2021 06:20:01 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 04 Mar 2021 06:23:20 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 04 Mar 2021 06:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Mar 2021 06:23:34 GMT
COPY file:52b881219ebb536dc2a07a100dc6c7e2307319ab3fee74c26c69db394fbb63eb in /usr/local/bin/ 
# Thu, 04 Mar 2021 06:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 06:23:46 GMT
EXPOSE 3306
# Thu, 04 Mar 2021 06:23:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6340e19a714d2edb6591a3c7a742db49afda548f15fb462e592a6c2f4783fbb6`  
		Last Modified: Mon, 22 Feb 2021 16:18:13 GMT  
		Size: 33.3 MB (33279996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b04c7047b52ebc24e2f93ba001030d6500a930738602afcd7d5b793cd0074`  
		Last Modified: Thu, 04 Mar 2021 03:02:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017db017688e47f4621a1ee72d3f358aed2f118ae88144b9453be0044dd8daf`  
		Last Modified: Thu, 04 Mar 2021 03:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0f8dc3847e2017060e5369ddd56fdc8e6d35859cf6ad4b0246e67321441c8`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc362fb4000733cf6190aec63f6d7fb70f7b56128e5742a02a8b793517f529`  
		Last Modified: Thu, 04 Mar 2021 06:54:26 GMT  
		Size: 6.7 MB (6667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8a654a1f08cb74bc479576aef5b11540041cef32816280b541f37d4bd127a`  
		Last Modified: Thu, 04 Mar 2021 06:54:25 GMT  
		Size: 1.2 MB (1244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1cfac5d8ea7113dedc0fe1bed30a9c8a24dd7c840a1671c4f2bbff082fdce`  
		Last Modified: Thu, 04 Mar 2021 06:54:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727839302f7c89cb483622bec898bd930c7e53a43c3eecaeec1a513fb7a8dbe`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 1.3 MB (1281016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805a247f143a691a38191d3dc464e13bc2f7ee0d226b1c8eaf35fab8a562a10`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe4d14164803804d46e336e0e4245ba4429507a82b2b5f5ce8c63b09e7b6f0`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd397924d0abb030c74b7bcf3278226d1778fde616391c61310d2b5e8a8efe3`  
		Last Modified: Thu, 04 Mar 2021 06:54:38 GMT  
		Size: 92.2 MB (92197337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f24958729d13b3776f19fad06281c372f14186544713521020efad84eb210`  
		Last Modified: Thu, 04 Mar 2021 06:54:19 GMT  
		Size: 5.0 KB (5033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
