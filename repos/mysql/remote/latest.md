## `mysql:latest`

```console
$ docker pull mysql@sha256:04ee7141256e83797ea4a84a4d31b1f1bc10111c8d1bc1879d52729ccd19e20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:bbeff35b63bf28aeb024de309aab2d501f8aa30e94664d3840d55b36c8db53c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161997667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0627ec6901db4b2aed6ca7ab35e43e19838ba079fffe8fe1be66b6feaad694de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 07:21:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 10 Apr 2021 07:21:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:21:50 GMT
ENV GOSU_VERSION=1.12
# Sat, 10 Apr 2021 07:22:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 10 Apr 2021 07:22:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 10 Apr 2021 07:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:22:14 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 10 Apr 2021 07:22:14 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 19 Apr 2021 18:56:30 GMT
ENV MYSQL_VERSION=8.0.24-1debian10
# Mon, 19 Apr 2021 18:56:31 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Mon, 19 Apr 2021 18:56:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 19 Apr 2021 18:56:45 GMT
VOLUME [/var/lib/mysql]
# Mon, 19 Apr 2021 18:56:45 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 19 Apr 2021 18:56:45 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 19 Apr 2021 18:56:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 19 Apr 2021 18:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Apr 2021 18:56:47 GMT
EXPOSE 3306 33060
# Mon, 19 Apr 2021 18:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444bb562699de912e7afcf6409615f9c0033118cc3aa35831d937a8d15e851c`  
		Last Modified: Sat, 10 Apr 2021 07:25:01 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4207b96940576ff42802b9c440bed0f1b5ef419c5a0c2576477776f217ef35`  
		Last Modified: Sat, 10 Apr 2021 07:25:02 GMT  
		Size: 4.2 MB (4179238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181cefd361ceae3da481ffcd156bd5b6e22f32a9345167199fe4773d70a6f133`  
		Last Modified: Sat, 10 Apr 2021 07:24:59 GMT  
		Size: 1.4 MB (1419407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2090759d8af87290c70a8a9cef4e7e894b800d55d069b8c4cf0bcd3a5d9f17`  
		Last Modified: Sat, 10 Apr 2021 07:24:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f235e0d7eefe6c5153946a57daebaf2d0744fb1d0676642f269554fc68ba2a`  
		Last Modified: Sat, 10 Apr 2021 07:25:02 GMT  
		Size: 13.4 MB (13447647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d870539cd9db00c747403f1d6c494a807052bce070f4ef243954b804a1ebb652`  
		Last Modified: Sat, 10 Apr 2021 07:24:58 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493aaa84617a809f6167a0b72fe986cf7b48a210e7fc31739f68a81b48f5def8`  
		Last Modified: Mon, 19 Apr 2021 18:57:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc0e534fc780f1c9db2a0b8b884b8b99a60e572734250f55cc400009202a2bd`  
		Last Modified: Mon, 19 Apr 2021 18:57:52 GMT  
		Size: 115.8 MB (115800999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae20d253f9d67774d118befce894e001b03a28fd23a1a6560d2cb3334af2a39`  
		Last Modified: Mon, 19 Apr 2021 18:57:34 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350664305b392bd62e77557c519551655ccd1409e786d6840f228445ae98f11`  
		Last Modified: Mon, 19 Apr 2021 18:57:34 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47da95a5aab06cf9a4a5a329c391e14fa433e1b064aa7175f89b9f6d57db4ea`  
		Last Modified: Mon, 19 Apr 2021 18:57:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
