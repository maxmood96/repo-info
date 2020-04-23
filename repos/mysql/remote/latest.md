## `mysql:latest`

```console
$ docker pull mysql@sha256:9643e9fbd6330d10686f8922292dcb20995e7b792c17d4e94ddf95255f1d5449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:09de7b17af0c17d397e6b69ff841756b80074aed00c1e91d7bc0f3caa5512113
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159104807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c27e8e5fcfab7805cfed996b55e5e98f43fd7ee76e1516f20cba139c6a299c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Thu, 23 Apr 2020 04:14:22 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Apr 2020 04:14:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Thu, 23 Apr 2020 04:14:52 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2020 04:14:52 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 23 Apr 2020 04:14:53 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Thu, 23 Apr 2020 04:14:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Apr 2020 04:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 04:14:55 GMT
EXPOSE 3306 33060
# Thu, 23 Apr 2020 04:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d4c3d31f9fc0ab35d93dc1903fbc323bffa08916d6e36bb1ff94daf7cfdaae`  
		Last Modified: Thu, 23 Apr 2020 04:17:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785bc90808da2b19e21a428ac3175392a1c8305895f511d5a0ab33860e449f0e`  
		Last Modified: Thu, 23 Apr 2020 04:17:58 GMT  
		Size: 113.0 MB (112955549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1339cf094729be360a598b68a79a4e7f4161e8f36cf3ae03c483be2c6e92edd5`  
		Last Modified: Thu, 23 Apr 2020 04:17:27 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb8f531cc379f34be8e909cb6ee7d80b4421550fef6eaf6f63e084870901b7f`  
		Last Modified: Thu, 23 Apr 2020 04:17:27 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b40c9f6a9184482286ab917d42eae90352f951adbebef03fcd100d9a3b55dff`  
		Last Modified: Thu, 23 Apr 2020 04:17:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
