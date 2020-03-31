## `mysql:latest`

```console
$ docker pull mysql@sha256:b69d0b62d02ee1eba8c7aeb32eba1bb678b6cfa4ccfb211a5d7931c7755dc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:fc84f426da06035a0de61789b4241db47db006efdc356286b5e28f4ce4bd38e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9228ee8bac7a8143818a7b028ee3386ea93e30a8f2e8bbf1440ca1ea3c26aa3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 31 Mar 2020 03:14:17 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Tue, 31 Mar 2020 03:14:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:14:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 31 Mar 2020 03:14:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:14:44 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 31 Mar 2020 03:14:44 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:14:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:14:46 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:14:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a808704d40c62b06667399c114521ef6a0a8422a8e54e277180edc80bce7bd9`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826517d075193cb62879b8fce405519b74092c2812a8a57d18e8e6b1661f71c2`  
		Last Modified: Tue, 31 Mar 2020 03:17:35 GMT  
		Size: 113.0 MB (112955573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd125db92884cb773d9e0d2038450821203c17b598e1585332a8dd3789d484`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c43b8c287976f0e6a323e1ca4ad6d1e85c9962d4a3ed7286668692d7849f9a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 5.1 KB (5075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811572b5ea5938f38eb7e8ec80b49861f7dc46f36945233ba100168b3cd3c6a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
