## `mysql:5-debian`

```console
$ docker pull mysql@sha256:c8b18d0e9ff97c0707b743a38329a26803eee9a15debfaf4dfab968430ff0040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:78f3af95aedf7d30dddb2fdfeb742364c92139176fcf281283921afda6698ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162526467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7234daae8b56ef0dd179a9b0ac1d3caabec8f5ec24b9b8c5fa5548726c48fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:29:20 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:29:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:29:27 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:29:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:29:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:29:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:29:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:29:43 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 13 Sep 2022 13:29:44 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Tue, 13 Sep 2022 13:29:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:30:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:30:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:30:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:30:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:30:04 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:30:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f00f90ab9fb1f6dec0aaed3222f9a223aafeb88ff89e928667798027e38fe`  
		Last Modified: Tue, 13 Sep 2022 13:31:20 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b02d67d09f246749165a2c4dbbec3379078626806dd176bc7b78e8063e794`  
		Last Modified: Tue, 13 Sep 2022 13:31:19 GMT  
		Size: 4.2 MB (4179268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8b4dde77ca39f886ba2341a799734289e0095dfc40e171cd0ebb4f57ef7ea3`  
		Last Modified: Tue, 13 Sep 2022 13:31:17 GMT  
		Size: 1.4 MB (1386727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0773e2457cfcbe7bf6cb7331dc96c5d8ad3057ec9ddc605edec86e23a850839`  
		Last Modified: Tue, 13 Sep 2022 13:31:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f6fbb5d95e91a9d9f23fb56f1b218898df14fbe68f849845c631e5c62cd7c4`  
		Last Modified: Tue, 13 Sep 2022 13:31:19 GMT  
		Size: 14.1 MB (14086589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76e91507063507d7f4ea92553f768c6c02f751e2abff5c79f0ecad4db84ea3c`  
		Last Modified: Tue, 13 Sep 2022 13:31:13 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd88e16698c47bbe0ebb35aaf608f4649130d229550c487ec076a1e7d365d9b2`  
		Last Modified: Tue, 13 Sep 2022 13:31:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd49ce6450ed5eff5d6dc4912fae13af570a6949117dcad8bd596aa2aac7fc8`  
		Last Modified: Tue, 13 Sep 2022 13:31:29 GMT  
		Size: 115.7 MB (115733145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aebff1d39a2e2c1b70d5f59b2ca4c480bb3fb7710fdd9c13de234b0888ca8f`  
		Last Modified: Tue, 13 Sep 2022 13:31:13 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530810f4aa2a3eb13c52d98896a08e72fc8778924dcfb1e078bfc396e9980034`  
		Last Modified: Tue, 13 Sep 2022 13:31:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
