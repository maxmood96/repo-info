<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.33`](#mysql5733)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.23`](#mysql8023)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:9fc60b229633ce1d1f2ee306705152d4b001056fb27c1b5debe23a732df72b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:c64d80f84bea7c8812e20b688a1ed127108cd4a871d48f81d55d3db37596e596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154589398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54bd1054823adac521a08c227f8f7106e93158184f0978eda0eb6ab7b4a5b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Tue, 09 Feb 2021 06:57:58 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:58:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:58:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Feb 2021 22:42:07 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:08 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66676c1ab9b3d426799a05289a12f402444cb42988a32f435443b25f912b71d4`  
		Last Modified: Tue, 09 Feb 2021 07:00:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebf78a38b634b1f06ebb79c28c6cb1ff23de8f78250559f52998ab046e451f`  
		Last Modified: Tue, 09 Feb 2021 07:00:47 GMT  
		Size: 108.4 MB (108439650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6510e5d6228331eaf1cb0c15479113fdf7cfdaec9971f600d5827faa64db511`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ca045d52c581ecd9a22452bdc39d058e43320c8fd814b8322d42250ede1823`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:6cacab35e5b6485621c20f54a27e3024965e5bebbd465edb5de8c5c556347392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:19fc1ff0d34a3373628f57137f700da9b8d703b51defecaa6f1e8127565868c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102977703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf1c71efa33776bdfb1d042776e1ddd82ab25da946d3eaf43329dc56050d94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:58:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:58:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:58:46 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:58:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:59:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:59:12 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:59:12 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 09 Feb 2021 06:59:12 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 09 Feb 2021 06:59:13 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:59:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:59:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Feb 2021 22:42:13 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:15 GMT
EXPOSE 3306
# Fri, 26 Feb 2021 22:42:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054a79d5f434643d85504f3fa669a7a2fd38b9d675e5ef9e2dc13065c8550e1`  
		Last Modified: Tue, 09 Feb 2021 07:00:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416bf57c90260d0c8e38fa2421456850c3f90fa813ba2b224b229097b8f643d3`  
		Last Modified: Tue, 09 Feb 2021 07:00:59 GMT  
		Size: 4.5 MB (4502219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c88503fb7a9b2d9f6926da73e7a0cb68344b0516a1ea93c82b471462bac8bb`  
		Last Modified: Tue, 09 Feb 2021 07:00:57 GMT  
		Size: 1.4 MB (1412094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5098f97b187ff5fadec59fda86a24d3c20afdb2d68c3dca4cac8ab021e9deb`  
		Last Modified: Tue, 09 Feb 2021 07:00:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed666c916387626331f555273381d24f1c5b863fda73ddaf78b432ec09994e7f`  
		Last Modified: Tue, 09 Feb 2021 07:01:03 GMT  
		Size: 10.2 MB (10224565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ed6d755e7543b3127a2eda1af380be399696d975486e1d87555e9d0d5817f9`  
		Last Modified: Tue, 09 Feb 2021 07:00:55 GMT  
		Size: 29.0 KB (28954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02f354a199cc1ec2858eff116bed29f1dd42e6f53ee90964623104e0e6f3d27`  
		Last Modified: Tue, 09 Feb 2021 07:00:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c73c04a085d851cae411a4d98cf862cae2e9afaa672f37837fc933050479fde`  
		Last Modified: Tue, 09 Feb 2021 07:01:15 GMT  
		Size: 64.3 MB (64273829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0321b62dc9a81a686e399008989d6fe924f37b9a3d544d07b8f7d54b60cd592a`  
		Last Modified: Fri, 26 Feb 2021 22:42:40 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520080f8d31717eb10d94ecf0be6cb6b7f9e7dd523acbcd77d2963c02f9f6d87`  
		Last Modified: Fri, 26 Feb 2021 22:42:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:6cacab35e5b6485621c20f54a27e3024965e5bebbd465edb5de8c5c556347392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:19fc1ff0d34a3373628f57137f700da9b8d703b51defecaa6f1e8127565868c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102977703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf1c71efa33776bdfb1d042776e1ddd82ab25da946d3eaf43329dc56050d94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:58:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:58:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:58:46 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:58:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:59:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:59:12 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:59:12 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 09 Feb 2021 06:59:12 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 09 Feb 2021 06:59:13 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:59:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:59:32 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Feb 2021 22:42:13 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:15 GMT
EXPOSE 3306
# Fri, 26 Feb 2021 22:42:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1054a79d5f434643d85504f3fa669a7a2fd38b9d675e5ef9e2dc13065c8550e1`  
		Last Modified: Tue, 09 Feb 2021 07:00:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416bf57c90260d0c8e38fa2421456850c3f90fa813ba2b224b229097b8f643d3`  
		Last Modified: Tue, 09 Feb 2021 07:00:59 GMT  
		Size: 4.5 MB (4502219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c88503fb7a9b2d9f6926da73e7a0cb68344b0516a1ea93c82b471462bac8bb`  
		Last Modified: Tue, 09 Feb 2021 07:00:57 GMT  
		Size: 1.4 MB (1412094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5098f97b187ff5fadec59fda86a24d3c20afdb2d68c3dca4cac8ab021e9deb`  
		Last Modified: Tue, 09 Feb 2021 07:00:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed666c916387626331f555273381d24f1c5b863fda73ddaf78b432ec09994e7f`  
		Last Modified: Tue, 09 Feb 2021 07:01:03 GMT  
		Size: 10.2 MB (10224565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ed6d755e7543b3127a2eda1af380be399696d975486e1d87555e9d0d5817f9`  
		Last Modified: Tue, 09 Feb 2021 07:00:55 GMT  
		Size: 29.0 KB (28954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02f354a199cc1ec2858eff116bed29f1dd42e6f53ee90964623104e0e6f3d27`  
		Last Modified: Tue, 09 Feb 2021 07:00:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c73c04a085d851cae411a4d98cf862cae2e9afaa672f37837fc933050479fde`  
		Last Modified: Tue, 09 Feb 2021 07:01:15 GMT  
		Size: 64.3 MB (64273829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0321b62dc9a81a686e399008989d6fe924f37b9a3d544d07b8f7d54b60cd592a`  
		Last Modified: Fri, 26 Feb 2021 22:42:40 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520080f8d31717eb10d94ecf0be6cb6b7f9e7dd523acbcd77d2963c02f9f6d87`  
		Last Modified: Fri, 26 Feb 2021 22:42:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:9fc60b229633ce1d1f2ee306705152d4b001056fb27c1b5debe23a732df72b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:c64d80f84bea7c8812e20b688a1ed127108cd4a871d48f81d55d3db37596e596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154589398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54bd1054823adac521a08c227f8f7106e93158184f0978eda0eb6ab7b4a5b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Tue, 09 Feb 2021 06:57:58 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:58:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:58:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Feb 2021 22:42:07 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:08 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66676c1ab9b3d426799a05289a12f402444cb42988a32f435443b25f912b71d4`  
		Last Modified: Tue, 09 Feb 2021 07:00:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebf78a38b634b1f06ebb79c28c6cb1ff23de8f78250559f52998ab046e451f`  
		Last Modified: Tue, 09 Feb 2021 07:00:47 GMT  
		Size: 108.4 MB (108439650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6510e5d6228331eaf1cb0c15479113fdf7cfdaec9971f600d5827faa64db511`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ca045d52c581ecd9a22452bdc39d058e43320c8fd814b8322d42250ede1823`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.33`

```console
$ docker pull mysql@sha256:9fc60b229633ce1d1f2ee306705152d4b001056fb27c1b5debe23a732df72b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.33` - linux; amd64

```console
$ docker pull mysql@sha256:c64d80f84bea7c8812e20b688a1ed127108cd4a871d48f81d55d3db37596e596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154589398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54bd1054823adac521a08c227f8f7106e93158184f0978eda0eb6ab7b4a5b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 09 Feb 2021 06:57:57 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Tue, 09 Feb 2021 06:57:58 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:58:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:58:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Feb 2021 22:42:07 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:08 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66676c1ab9b3d426799a05289a12f402444cb42988a32f435443b25f912b71d4`  
		Last Modified: Tue, 09 Feb 2021 07:00:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebf78a38b634b1f06ebb79c28c6cb1ff23de8f78250559f52998ab046e451f`  
		Last Modified: Tue, 09 Feb 2021 07:00:47 GMT  
		Size: 108.4 MB (108439650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6510e5d6228331eaf1cb0c15479113fdf7cfdaec9971f600d5827faa64db511`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ca045d52c581ecd9a22452bdc39d058e43320c8fd814b8322d42250ede1823`  
		Last Modified: Fri, 26 Feb 2021 22:42:35 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:7706e4c382be813b58ef514f2bdac747cd463a6866c6c81165d42a1d0e4fe947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:03306a1f248727ec979f61424c5fb5150e2c5fd2436f2561c5259b1258d6063c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159259013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8457e9155715d4e1c80c9e048d94c9b47b5b733fa927756280382dd326403644`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Tue, 09 Feb 2021 06:57:23 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:57:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:57:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 09 Feb 2021 06:57:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 26 Feb 2021 22:42:01 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:02 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7599a246fd60f5d0c384dc4e060813410f37e58f63e0f623df7b99d17f212d1`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a55bf0c196d923dd598efe8bc1e1d942ad9b9e166d74eebf83e64cda96b336`  
		Last Modified: Tue, 09 Feb 2021 07:00:16 GMT  
		Size: 113.1 MB (113108416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ac54f4c47df421ad19e780229010e41105211a3bf4a0206d21135aa34d892`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ddd5d1b5434f1163befba0e098adcd39d884f807b29d292da0a7c4ed293b0b`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aefd67cb33d07c00f83cfd8a20cd3fb69984201836caa9d178e7fda4eec2d95`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:7706e4c382be813b58ef514f2bdac747cd463a6866c6c81165d42a1d0e4fe947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:03306a1f248727ec979f61424c5fb5150e2c5fd2436f2561c5259b1258d6063c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159259013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8457e9155715d4e1c80c9e048d94c9b47b5b733fa927756280382dd326403644`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Tue, 09 Feb 2021 06:57:23 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:57:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:57:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 09 Feb 2021 06:57:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 26 Feb 2021 22:42:01 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:02 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7599a246fd60f5d0c384dc4e060813410f37e58f63e0f623df7b99d17f212d1`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a55bf0c196d923dd598efe8bc1e1d942ad9b9e166d74eebf83e64cda96b336`  
		Last Modified: Tue, 09 Feb 2021 07:00:16 GMT  
		Size: 113.1 MB (113108416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ac54f4c47df421ad19e780229010e41105211a3bf4a0206d21135aa34d892`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ddd5d1b5434f1163befba0e098adcd39d884f807b29d292da0a7c4ed293b0b`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aefd67cb33d07c00f83cfd8a20cd3fb69984201836caa9d178e7fda4eec2d95`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.23`

```console
$ docker pull mysql@sha256:7706e4c382be813b58ef514f2bdac747cd463a6866c6c81165d42a1d0e4fe947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.23` - linux; amd64

```console
$ docker pull mysql@sha256:03306a1f248727ec979f61424c5fb5150e2c5fd2436f2561c5259b1258d6063c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159259013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8457e9155715d4e1c80c9e048d94c9b47b5b733fa927756280382dd326403644`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Tue, 09 Feb 2021 06:57:23 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:57:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:57:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 09 Feb 2021 06:57:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 26 Feb 2021 22:42:01 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:02 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7599a246fd60f5d0c384dc4e060813410f37e58f63e0f623df7b99d17f212d1`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a55bf0c196d923dd598efe8bc1e1d942ad9b9e166d74eebf83e64cda96b336`  
		Last Modified: Tue, 09 Feb 2021 07:00:16 GMT  
		Size: 113.1 MB (113108416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ac54f4c47df421ad19e780229010e41105211a3bf4a0206d21135aa34d892`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ddd5d1b5434f1163befba0e098adcd39d884f807b29d292da0a7c4ed293b0b`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aefd67cb33d07c00f83cfd8a20cd3fb69984201836caa9d178e7fda4eec2d95`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:7706e4c382be813b58ef514f2bdac747cd463a6866c6c81165d42a1d0e4fe947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:03306a1f248727ec979f61424c5fb5150e2c5fd2436f2561c5259b1258d6063c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159259013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8457e9155715d4e1c80c9e048d94c9b47b5b733fa927756280382dd326403644`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:56:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Feb 2021 06:57:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Feb 2021 06:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Feb 2021 06:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Feb 2021 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:57:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 09 Feb 2021 06:57:22 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Tue, 09 Feb 2021 06:57:23 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Feb 2021 06:57:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 09 Feb 2021 06:57:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 09 Feb 2021 06:57:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 26 Feb 2021 22:42:01 GMT
COPY file:74c3ab1ae4fa929ca3dc5f3cc1e9d17cad9e3b3c8bdfdc747b12bfa93d45389f in /usr/local/bin/ 
# Fri, 26 Feb 2021 22:42:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Feb 2021 22:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Feb 2021 22:42:02 GMT
EXPOSE 3306 33060
# Fri, 26 Feb 2021 22:42:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f790bd91da3aa0013461d5759e463512d8b28cbcc6019d947cbc2430234124`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ae51788e9a0f5f74a350a9510b0c34a75cb140b19fccfb937048ad2685c53`  
		Last Modified: Tue, 09 Feb 2021 06:59:56 GMT  
		Size: 4.2 MB (4178308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb9439d751502b82c88ec63defe03aa162910d8aa3abc1e6d61e1cc9f1ab78`  
		Last Modified: Tue, 09 Feb 2021 06:59:55 GMT  
		Size: 1.4 MB (1419363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c7fe16c78e47c96158f154f3c15659175be81e139625ee182107bd98ae290`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698058ef136cda4bbf459e90bb414a8a82b57ddb2c0ad08a1fa602fb169d2899`  
		Last Modified: Tue, 09 Feb 2021 06:59:58 GMT  
		Size: 13.4 MB (13447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4690143a669ebe32feb24774fe6ad4f1dd321d18a2364723ce9d9df19b732878`  
		Last Modified: Tue, 09 Feb 2021 06:59:54 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7599a246fd60f5d0c384dc4e060813410f37e58f63e0f623df7b99d17f212d1`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a55bf0c196d923dd598efe8bc1e1d942ad9b9e166d74eebf83e64cda96b336`  
		Last Modified: Tue, 09 Feb 2021 07:00:16 GMT  
		Size: 113.1 MB (113108416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ac54f4c47df421ad19e780229010e41105211a3bf4a0206d21135aa34d892`  
		Last Modified: Tue, 09 Feb 2021 06:59:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ddd5d1b5434f1163befba0e098adcd39d884f807b29d292da0a7c4ed293b0b`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aefd67cb33d07c00f83cfd8a20cd3fb69984201836caa9d178e7fda4eec2d95`  
		Last Modified: Fri, 26 Feb 2021 22:42:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
