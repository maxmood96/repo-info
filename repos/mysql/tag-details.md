<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.48`](#mysql5648)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.30`](#mysql5730)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.20`](#mysql8020)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:e4d39b85118358ffef6adc5e8c7d00e49d20b25597e6ffdc994696f10e3dc8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:7eab7393cf42c596b8491e6b3d6931eb116e998e2307bb7901b0379a4d36bf5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154399513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73346bdf4656bb61e3d36ccfb1ea0f9eb003657ba6afab44cda56b246531126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:41:16 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 14 May 2020 03:41:17 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Thu, 14 May 2020 03:41:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 14 May 2020 03:41:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:53 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:55 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37958cbebcf059376e604f563728d0071b6adf93fcf1129e6567c307d5010a5`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04960017f638d43bb0d0fcb27a2272b057109a91f62f72226a9a2faa15265b1d`  
		Last Modified: Thu, 14 May 2020 03:44:44 GMT  
		Size: 108.3 MB (108257072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1285def0d2a2b98eb29dca584a7fbc18317dd921bcfe76bdde04671ba946166`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670cb3a9678e452d30c8da6585971277eee24a0d39d683bf92e36f49dc6fe051`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:8366c5962d962160f5da37dcd89e2a8e5b879f3843895cbeab2b953f6e2a520d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:4b32ed623e41edc3a53946b94bb8bbe29edcecadbc18d68bb7897b2dc44b91b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5880e7d0e676513bf66cba523ef44e936fce3050f9063312812f1f0c7b54d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:23:54 GMT
ADD file:3e0b81347262efc5a7401a531be7ab45cb8ab05ddab528fbb849bea0053865a0 in / 
# Wed, 13 May 2020 21:23:54 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:42:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:42:14 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:42:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:42:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:42:49 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:42:49 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 14 May 2020 03:42:49 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Thu, 14 May 2020 03:42:51 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:43:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 14 May 2020 03:43:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:43:14 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:43:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:43:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:43:16 GMT
EXPOSE 3306
# Thu, 14 May 2020 03:43:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4f2068f62324fe92e80c472afb3742bf506f2a52712bf36ec0456de94c5b14e`  
		Last Modified: Wed, 13 May 2020 21:30:12 GMT  
		Size: 22.5 MB (22513438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ed3094f754ca29cfd096e78ebed456641cfe1214433af8436e168da2eb33c3`  
		Last Modified: Thu, 14 May 2020 03:44:55 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd97809f887f438eea8a920593bffd0226b35851d9ed8e2e400651733540b14`  
		Last Modified: Thu, 14 May 2020 03:44:55 GMT  
		Size: 4.5 MB (4501259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8713d901367625c6ed205c12958111639296f345c237b85f5a95534fcfd8b`  
		Last Modified: Thu, 14 May 2020 03:44:54 GMT  
		Size: 1.4 MB (1412339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fc6b055cf83d77b770e03e0b80e19bbaaad61f82749d13008e44dd6ec4fac4`  
		Last Modified: Thu, 14 May 2020 03:44:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa07d5334fd05067dfc785fbda04d769fc54f53446c46e7bae2ea8cb7751919`  
		Last Modified: Thu, 14 May 2020 03:44:57 GMT  
		Size: 10.2 MB (10223048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af37b57ec4fafdd7f689fa930da7b06d7639bb1bee762a73028bf43c7813f4`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040e5624a3301e632a4e53bb3c4be70f388eac7315da129d91407cab5bfe8c4b`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756ca6a4cae738560a939319c9d9302851356114907e434791152c199a6690d`  
		Last Modified: Thu, 14 May 2020 03:45:06 GMT  
		Size: 64.2 MB (64195249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec995520f1fb23fbc5172437d35c461256e814ad55004c5b8ef71e7ca73b602`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 5.2 KB (5151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87ee36f6ac04f9a7cee263d9acef424682afa3ca4ef6791b74e024f1b756b36`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.48`

```console
$ docker pull mysql@sha256:8366c5962d962160f5da37dcd89e2a8e5b879f3843895cbeab2b953f6e2a520d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.48` - linux; amd64

```console
$ docker pull mysql@sha256:4b32ed623e41edc3a53946b94bb8bbe29edcecadbc18d68bb7897b2dc44b91b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5880e7d0e676513bf66cba523ef44e936fce3050f9063312812f1f0c7b54d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:23:54 GMT
ADD file:3e0b81347262efc5a7401a531be7ab45cb8ab05ddab528fbb849bea0053865a0 in / 
# Wed, 13 May 2020 21:23:54 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:42:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:42:14 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:42:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:42:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:42:49 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:42:49 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 14 May 2020 03:42:49 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Thu, 14 May 2020 03:42:51 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:43:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 14 May 2020 03:43:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:43:14 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:43:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:43:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:43:16 GMT
EXPOSE 3306
# Thu, 14 May 2020 03:43:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4f2068f62324fe92e80c472afb3742bf506f2a52712bf36ec0456de94c5b14e`  
		Last Modified: Wed, 13 May 2020 21:30:12 GMT  
		Size: 22.5 MB (22513438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ed3094f754ca29cfd096e78ebed456641cfe1214433af8436e168da2eb33c3`  
		Last Modified: Thu, 14 May 2020 03:44:55 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd97809f887f438eea8a920593bffd0226b35851d9ed8e2e400651733540b14`  
		Last Modified: Thu, 14 May 2020 03:44:55 GMT  
		Size: 4.5 MB (4501259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8713d901367625c6ed205c12958111639296f345c237b85f5a95534fcfd8b`  
		Last Modified: Thu, 14 May 2020 03:44:54 GMT  
		Size: 1.4 MB (1412339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fc6b055cf83d77b770e03e0b80e19bbaaad61f82749d13008e44dd6ec4fac4`  
		Last Modified: Thu, 14 May 2020 03:44:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa07d5334fd05067dfc785fbda04d769fc54f53446c46e7bae2ea8cb7751919`  
		Last Modified: Thu, 14 May 2020 03:44:57 GMT  
		Size: 10.2 MB (10223048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af37b57ec4fafdd7f689fa930da7b06d7639bb1bee762a73028bf43c7813f4`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040e5624a3301e632a4e53bb3c4be70f388eac7315da129d91407cab5bfe8c4b`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756ca6a4cae738560a939319c9d9302851356114907e434791152c199a6690d`  
		Last Modified: Thu, 14 May 2020 03:45:06 GMT  
		Size: 64.2 MB (64195249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec995520f1fb23fbc5172437d35c461256e814ad55004c5b8ef71e7ca73b602`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 5.2 KB (5151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87ee36f6ac04f9a7cee263d9acef424682afa3ca4ef6791b74e024f1b756b36`  
		Last Modified: Thu, 14 May 2020 03:44:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:e4d39b85118358ffef6adc5e8c7d00e49d20b25597e6ffdc994696f10e3dc8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:7eab7393cf42c596b8491e6b3d6931eb116e998e2307bb7901b0379a4d36bf5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154399513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73346bdf4656bb61e3d36ccfb1ea0f9eb003657ba6afab44cda56b246531126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:41:16 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 14 May 2020 03:41:17 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Thu, 14 May 2020 03:41:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 14 May 2020 03:41:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:53 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:55 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37958cbebcf059376e604f563728d0071b6adf93fcf1129e6567c307d5010a5`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04960017f638d43bb0d0fcb27a2272b057109a91f62f72226a9a2faa15265b1d`  
		Last Modified: Thu, 14 May 2020 03:44:44 GMT  
		Size: 108.3 MB (108257072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1285def0d2a2b98eb29dca584a7fbc18317dd921bcfe76bdde04671ba946166`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670cb3a9678e452d30c8da6585971277eee24a0d39d683bf92e36f49dc6fe051`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.30`

```console
$ docker pull mysql@sha256:e4d39b85118358ffef6adc5e8c7d00e49d20b25597e6ffdc994696f10e3dc8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.30` - linux; amd64

```console
$ docker pull mysql@sha256:7eab7393cf42c596b8491e6b3d6931eb116e998e2307bb7901b0379a4d36bf5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154399513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73346bdf4656bb61e3d36ccfb1ea0f9eb003657ba6afab44cda56b246531126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:41:16 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 14 May 2020 03:41:17 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Thu, 14 May 2020 03:41:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 14 May 2020 03:41:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:53 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:55 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37958cbebcf059376e604f563728d0071b6adf93fcf1129e6567c307d5010a5`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04960017f638d43bb0d0fcb27a2272b057109a91f62f72226a9a2faa15265b1d`  
		Last Modified: Thu, 14 May 2020 03:44:44 GMT  
		Size: 108.3 MB (108257072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1285def0d2a2b98eb29dca584a7fbc18317dd921bcfe76bdde04671ba946166`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670cb3a9678e452d30c8da6585971277eee24a0d39d683bf92e36f49dc6fe051`  
		Last Modified: Thu, 14 May 2020 03:44:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:dc255ca50a42b3589197000b1f9bab2b4e010158d1a9f56c3db6ee145506f625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:c0db9c67684a006330ce08aaf6af4367f94dd5eeda4673e5fca2210eccfdb8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157629927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4d95e478ff2962ede50c50b7dc2fc699382bcb94ad301e9c6805609f0939a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:40:35 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 14 May 2020 03:40:36 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Thu, 14 May 2020 03:40:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Thu, 14 May 2020 03:41:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:05 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 14 May 2020 03:41:06 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:08 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1e55059a95bebc5ebc063313e660cc44d6c92544f980034464403d2b45bcf3`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd29a0dcde84a30991ec2f0527fc88735e84283e41c0d56107838af4654fcef`  
		Last Modified: Thu, 14 May 2020 03:44:01 GMT  
		Size: 111.5 MB (111486588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a001c6ec749de3ccb9312a432d1cb32ac290fa66bc0746463fdc1272794b9`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77cbeb422bbd0e835a5cc2bb8a76bf3845a5995a424341e200bcfb7be0e6cc`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35cdbd42ccff6610c35183a013370a5fba4c372c0fd8a09838caed0d93e156`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:dc255ca50a42b3589197000b1f9bab2b4e010158d1a9f56c3db6ee145506f625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:c0db9c67684a006330ce08aaf6af4367f94dd5eeda4673e5fca2210eccfdb8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157629927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4d95e478ff2962ede50c50b7dc2fc699382bcb94ad301e9c6805609f0939a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:40:35 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 14 May 2020 03:40:36 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Thu, 14 May 2020 03:40:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Thu, 14 May 2020 03:41:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:05 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 14 May 2020 03:41:06 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:08 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1e55059a95bebc5ebc063313e660cc44d6c92544f980034464403d2b45bcf3`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd29a0dcde84a30991ec2f0527fc88735e84283e41c0d56107838af4654fcef`  
		Last Modified: Thu, 14 May 2020 03:44:01 GMT  
		Size: 111.5 MB (111486588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a001c6ec749de3ccb9312a432d1cb32ac290fa66bc0746463fdc1272794b9`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77cbeb422bbd0e835a5cc2bb8a76bf3845a5995a424341e200bcfb7be0e6cc`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35cdbd42ccff6610c35183a013370a5fba4c372c0fd8a09838caed0d93e156`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.20`

```console
$ docker pull mysql@sha256:dc255ca50a42b3589197000b1f9bab2b4e010158d1a9f56c3db6ee145506f625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.20` - linux; amd64

```console
$ docker pull mysql@sha256:c0db9c67684a006330ce08aaf6af4367f94dd5eeda4673e5fca2210eccfdb8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157629927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4d95e478ff2962ede50c50b7dc2fc699382bcb94ad301e9c6805609f0939a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:40:35 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 14 May 2020 03:40:36 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Thu, 14 May 2020 03:40:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Thu, 14 May 2020 03:41:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:05 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 14 May 2020 03:41:06 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:08 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1e55059a95bebc5ebc063313e660cc44d6c92544f980034464403d2b45bcf3`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd29a0dcde84a30991ec2f0527fc88735e84283e41c0d56107838af4654fcef`  
		Last Modified: Thu, 14 May 2020 03:44:01 GMT  
		Size: 111.5 MB (111486588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a001c6ec749de3ccb9312a432d1cb32ac290fa66bc0746463fdc1272794b9`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77cbeb422bbd0e835a5cc2bb8a76bf3845a5995a424341e200bcfb7be0e6cc`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35cdbd42ccff6610c35183a013370a5fba4c372c0fd8a09838caed0d93e156`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:dc255ca50a42b3589197000b1f9bab2b4e010158d1a9f56c3db6ee145506f625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c0db9c67684a006330ce08aaf6af4367f94dd5eeda4673e5fca2210eccfdb8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157629927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4d95e478ff2962ede50c50b7dc2fc699382bcb94ad301e9c6805609f0939a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:40:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 14 May 2020 03:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:09 GMT
ENV GOSU_VERSION=1.12
# Thu, 14 May 2020 03:40:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 14 May 2020 03:40:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 14 May 2020 03:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:40:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 14 May 2020 03:40:35 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 14 May 2020 03:40:36 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Thu, 14 May 2020 03:40:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 14 May 2020 03:41:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Thu, 14 May 2020 03:41:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 14 May 2020 03:41:05 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 14 May 2020 03:41:06 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 14 May 2020 03:41:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 14 May 2020 03:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2020 03:41:08 GMT
EXPOSE 3306 33060
# Thu, 14 May 2020 03:41:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7d6a8a868a3155126b5e3a70cf9f8eb526a9f95145ffcd92447599fef5cee`  
		Last Modified: Thu, 14 May 2020 03:43:43 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9468923105247b19ba41b9677ab5499fe46ec09896d902a59e6f68b48e4aa`  
		Last Modified: Thu, 14 May 2020 03:43:42 GMT  
		Size: 4.2 MB (4178103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f4d07efa543389313cf79b9ddf006c03f89ae790b42c6ae5eaf7715a8c2b7`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 1.4 MB (1419312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d396a6205778a07c929e6b08dd0545d4eaa0ac6fe92f4a18e98ffb42cc85b`  
		Last Modified: Thu, 14 May 2020 03:43:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2b93048f0d72fd5b8ea38cf7fa24b32807815c540e2d44d6bf40609687b2`  
		Last Modified: Thu, 14 May 2020 03:43:44 GMT  
		Size: 13.4 MB (13443319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530904b4a8b7024de7f12c75b467a3137e8d7d8f55f4dfd8257d18a5fe619621`  
		Last Modified: Thu, 14 May 2020 03:43:40 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1e55059a95bebc5ebc063313e660cc44d6c92544f980034464403d2b45bcf3`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd29a0dcde84a30991ec2f0527fc88735e84283e41c0d56107838af4654fcef`  
		Last Modified: Thu, 14 May 2020 03:44:01 GMT  
		Size: 111.5 MB (111486588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a001c6ec749de3ccb9312a432d1cb32ac290fa66bc0746463fdc1272794b9`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77cbeb422bbd0e835a5cc2bb8a76bf3845a5995a424341e200bcfb7be0e6cc`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35cdbd42ccff6610c35183a013370a5fba4c372c0fd8a09838caed0d93e156`  
		Last Modified: Thu, 14 May 2020 03:43:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
