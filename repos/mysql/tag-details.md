<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.39`](#mysql5739)
-	[`mysql:5.7.39-debian`](#mysql5739-debian)
-	[`mysql:5.7.39-oracle`](#mysql5739-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.30`](#mysql8030)
-	[`mysql:8.0.30-debian`](#mysql8030-debian)
-	[`mysql:8.0.30-oracle`](#mysql8030-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:c8b18d0e9ff97c0707b743a38329a26803eee9a15debfaf4dfab968430ff0040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

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

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39-debian`

```console
$ docker pull mysql@sha256:c8b18d0e9ff97c0707b743a38329a26803eee9a15debfaf4dfab968430ff0040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-debian` - linux; amd64

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

## `mysql:5.7.39-oracle`

```console
$ docker pull mysql@sha256:c1bda6ecdbc63d3b0d3a3a3ce195de3dd755c4a0658ed782a16a0682216b9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:933bcfdb15aa93f4cfc0dad61da7e88652a3e87d6b69cf87ecbde22226ed5e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128314571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff57b7d2d1e009d0b271972f62dbf4de64b8cdb9cd646442aeda961e615f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:03:20 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 Aug 2022 23:03:21 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 23:03:23 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 23:03:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 24 Aug 2022 23:03:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 24 Aug 2022 23:03:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Wed, 24 Aug 2022 23:03:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 Aug 2022 23:03:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 Aug 2022 23:04:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 Aug 2022 23:04:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Wed, 24 Aug 2022 23:04:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 24 Aug 2022 23:04:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 23:04:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:04:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 Aug 2022 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:04:23 GMT
EXPOSE 3306 33060
# Wed, 24 Aug 2022 23:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cb6fccbfd4176deef1152906dbc36d145ec1dddbfab9dc9a8d03adb93f9d0`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63612353671c1c6829c0e3a53459b2721fd28aa819d3aeb8d21ad6939dc215a`  
		Last Modified: Wed, 24 Aug 2022 23:05:49 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447901201612ee3db925aaf3a9d4109fb3ad8d8f673f2122ffbc87a0157ce79e`  
		Last Modified: Wed, 24 Aug 2022 23:05:47 GMT  
		Size: 4.5 MB (4542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bc806cc29ced38232ba7ea23663518c2fafc12584fe2a709ab9a7871a4dd3`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ec1f4b3b0d9993c7b0c0fc8497e123d028f7bd0cf87e018340508f47e6f04d`  
		Last Modified: Wed, 24 Aug 2022 23:05:46 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ed1eb2fd4f8f76f3550bd1c47dacf2b482a208e0e3cf295dfc51be4adb141`  
		Last Modified: Wed, 24 Aug 2022 23:05:48 GMT  
		Size: 25.5 MB (25496458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbde3edd97c41a8d9d492f0556e8f9d86d9df5026fccb549247adc48ecc812`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5aa35cc1546ad21bdc5184b882985259f75ec2890c6a076dcde821a3695b84`  
		Last Modified: Wed, 24 Aug 2022 23:05:53 GMT  
		Size: 48.6 MB (48608531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c92bf6471bf0717f1bd0ba277d6fcc96bc47df3330ad0480dce9ed3526d31a`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b80de0d1af3dcd626ab10baf2e5089ecdda0ed847761f504f7a16087936653`  
		Last Modified: Wed, 24 Aug 2022 23:05:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:9e0bdb3b54035e8deb547fd0291b21762c86669bd48f5b4819c079c94c425816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2506c5888811a468d1bb01f18ef37a7a13847122c7e48e9ad1ba013b9b8c52fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157873370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119434801ff2d09c0f7cc72bff23e5876109309b189302c59b40d38ec736f245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:28:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:28:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:28:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 13 Sep 2022 13:28:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:29:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:29:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:29:13 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 13 Sep 2022 13:29:14 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:29:14 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:29:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c5efc42d0a2eac340f0b7f83239cdd89743a262660794b6b4125048bf6d67`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb3aa78cebf34a1c1dcac56576d08c293736a9e5d2af49d4abcf74717eb936`  
		Last Modified: Tue, 13 Sep 2022 13:30:39 GMT  
		Size: 4.4 MB (4414806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3edf2bce1ded759b2621e3f9b6d08c0aaa774b41d0a75644723e75c18333f5`  
		Last Modified: Tue, 13 Sep 2022 13:30:37 GMT  
		Size: 1.4 MB (1418436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e9b048283778fc1730490adba5e9108c9d2be7ec217bca6d2aae6147a5409c`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef175ef2e26b0a73ffc1e4139460ac9857413163333b0b48cd4ebae090a6c23`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 12.7 MB (12661855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805f7502c031da7089f62f19829407ae4d4e28609461b6c797d8e8c6469b651`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7ff40073185d68c0e971013dadecaec0807d064de3ea39c696ff1522aa336`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dfbd1dbaeca6ed4bb7011a37155a4b41169b2ac8b51190a2eeb3117edf624`  
		Last Modified: Tue, 13 Sep 2022 13:30:50 GMT  
		Size: 108.0 MB (107963119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b8ebac2e8391238177c2f59bb38c87d62578f4105192dfdd480c575fba1e3`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c758363844a5d6c01628e945d14648ae844cb9d4a75f6d162557b372d626730`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663382eaa47c2752415ea0b14d4ad4fe670882ad23493f48d5434a83ed9276c`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9e0bdb3b54035e8deb547fd0291b21762c86669bd48f5b4819c079c94c425816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2506c5888811a468d1bb01f18ef37a7a13847122c7e48e9ad1ba013b9b8c52fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157873370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119434801ff2d09c0f7cc72bff23e5876109309b189302c59b40d38ec736f245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:28:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:28:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:28:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 13 Sep 2022 13:28:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:29:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:29:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:29:13 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 13 Sep 2022 13:29:14 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:29:14 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:29:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c5efc42d0a2eac340f0b7f83239cdd89743a262660794b6b4125048bf6d67`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb3aa78cebf34a1c1dcac56576d08c293736a9e5d2af49d4abcf74717eb936`  
		Last Modified: Tue, 13 Sep 2022 13:30:39 GMT  
		Size: 4.4 MB (4414806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3edf2bce1ded759b2621e3f9b6d08c0aaa774b41d0a75644723e75c18333f5`  
		Last Modified: Tue, 13 Sep 2022 13:30:37 GMT  
		Size: 1.4 MB (1418436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e9b048283778fc1730490adba5e9108c9d2be7ec217bca6d2aae6147a5409c`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef175ef2e26b0a73ffc1e4139460ac9857413163333b0b48cd4ebae090a6c23`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 12.7 MB (12661855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805f7502c031da7089f62f19829407ae4d4e28609461b6c797d8e8c6469b651`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7ff40073185d68c0e971013dadecaec0807d064de3ea39c696ff1522aa336`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dfbd1dbaeca6ed4bb7011a37155a4b41169b2ac8b51190a2eeb3117edf624`  
		Last Modified: Tue, 13 Sep 2022 13:30:50 GMT  
		Size: 108.0 MB (107963119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b8ebac2e8391238177c2f59bb38c87d62578f4105192dfdd480c575fba1e3`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c758363844a5d6c01628e945d14648ae844cb9d4a75f6d162557b372d626730`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663382eaa47c2752415ea0b14d4ad4fe670882ad23493f48d5434a83ed9276c`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-debian`

```console
$ docker pull mysql@sha256:9e0bdb3b54035e8deb547fd0291b21762c86669bd48f5b4819c079c94c425816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.30-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2506c5888811a468d1bb01f18ef37a7a13847122c7e48e9ad1ba013b9b8c52fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157873370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119434801ff2d09c0f7cc72bff23e5876109309b189302c59b40d38ec736f245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:28:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:28:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:28:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 13 Sep 2022 13:28:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:29:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:29:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:29:13 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 13 Sep 2022 13:29:14 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:29:14 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:29:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c5efc42d0a2eac340f0b7f83239cdd89743a262660794b6b4125048bf6d67`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb3aa78cebf34a1c1dcac56576d08c293736a9e5d2af49d4abcf74717eb936`  
		Last Modified: Tue, 13 Sep 2022 13:30:39 GMT  
		Size: 4.4 MB (4414806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3edf2bce1ded759b2621e3f9b6d08c0aaa774b41d0a75644723e75c18333f5`  
		Last Modified: Tue, 13 Sep 2022 13:30:37 GMT  
		Size: 1.4 MB (1418436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e9b048283778fc1730490adba5e9108c9d2be7ec217bca6d2aae6147a5409c`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef175ef2e26b0a73ffc1e4139460ac9857413163333b0b48cd4ebae090a6c23`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 12.7 MB (12661855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805f7502c031da7089f62f19829407ae4d4e28609461b6c797d8e8c6469b651`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7ff40073185d68c0e971013dadecaec0807d064de3ea39c696ff1522aa336`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dfbd1dbaeca6ed4bb7011a37155a4b41169b2ac8b51190a2eeb3117edf624`  
		Last Modified: Tue, 13 Sep 2022 13:30:50 GMT  
		Size: 108.0 MB (107963119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b8ebac2e8391238177c2f59bb38c87d62578f4105192dfdd480c575fba1e3`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c758363844a5d6c01628e945d14648ae844cb9d4a75f6d162557b372d626730`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663382eaa47c2752415ea0b14d4ad4fe670882ad23493f48d5434a83ed9276c`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-oracle`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:9e0bdb3b54035e8deb547fd0291b21762c86669bd48f5b4819c079c94c425816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:2506c5888811a468d1bb01f18ef37a7a13847122c7e48e9ad1ba013b9b8c52fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157873370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119434801ff2d09c0f7cc72bff23e5876109309b189302c59b40d38ec736f245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:28:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:28:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:28:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 13 Sep 2022 13:28:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:29:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:29:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:29:13 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 13 Sep 2022 13:29:14 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:29:14 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:29:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c5efc42d0a2eac340f0b7f83239cdd89743a262660794b6b4125048bf6d67`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb3aa78cebf34a1c1dcac56576d08c293736a9e5d2af49d4abcf74717eb936`  
		Last Modified: Tue, 13 Sep 2022 13:30:39 GMT  
		Size: 4.4 MB (4414806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3edf2bce1ded759b2621e3f9b6d08c0aaa774b41d0a75644723e75c18333f5`  
		Last Modified: Tue, 13 Sep 2022 13:30:37 GMT  
		Size: 1.4 MB (1418436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e9b048283778fc1730490adba5e9108c9d2be7ec217bca6d2aae6147a5409c`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef175ef2e26b0a73ffc1e4139460ac9857413163333b0b48cd4ebae090a6c23`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 12.7 MB (12661855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805f7502c031da7089f62f19829407ae4d4e28609461b6c797d8e8c6469b651`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7ff40073185d68c0e971013dadecaec0807d064de3ea39c696ff1522aa336`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dfbd1dbaeca6ed4bb7011a37155a4b41169b2ac8b51190a2eeb3117edf624`  
		Last Modified: Tue, 13 Sep 2022 13:30:50 GMT  
		Size: 108.0 MB (107963119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b8ebac2e8391238177c2f59bb38c87d62578f4105192dfdd480c575fba1e3`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c758363844a5d6c01628e945d14648ae844cb9d4a75f6d162557b372d626730`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663382eaa47c2752415ea0b14d4ad4fe670882ad23493f48d5434a83ed9276c`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:cdf3b62d78d1bbb1d2bd6716895a84014e00716177cbb7e90f6c6a37a21dc796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:713a3c26c5130f06fe17b16b314f1058f9efeb07330164da0e81d97d5a57d50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132821978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3b5098b416cc4294d8d5c43c2f0f8251e91711347318e73cb290ffe2783bcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:36:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:36:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:36:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:37:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:37:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:37:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:37:19 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:37:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:37:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:37:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:37:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:38:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:38:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:38:22 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:38:23 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:38:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20050901c93a392b4d869f72c17aeac0f66a915beba685fd4aa2997f902da`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a5e171c2f8a6102de2042eefcc2bd2d4350ac908a05e5fa8bbb8794c0c4962`  
		Last Modified: Tue, 30 Aug 2022 21:39:03 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cedd8aa0612db19ab26bc7c679dec813250a37cb859d0400174e04a64cd961`  
		Last Modified: Tue, 30 Aug 2022 21:39:02 GMT  
		Size: 4.6 MB (4613881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a485af4cc99d96770f4daf154caa1f380c837288c6bcf976343f66a59ee156`  
		Last Modified: Tue, 30 Aug 2022 21:39:01 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16a57baf60e7bb26e47188758d411059af655825a32e973cb109355346f8ca`  
		Last Modified: Tue, 30 Aug 2022 21:39:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bab9180d2a34048d477c84eb81a2c6b62688f73a430460afc37c9722f94a89`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 47.7 MB (47743357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aceb7e4f48a81a87f7ffff04fdb7acc67d6f518d1d002f702bdf94d9463ed4`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269002e5cf588450df92e5c72134c446d03e9716868dd465a03b6285f647ff5d`  
		Last Modified: Tue, 30 Aug 2022 21:39:06 GMT  
		Size: 40.0 MB (40004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abeb1bd18ef4adbffff839316437d7d316dac712ea03169f9aa7ee40013422`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd79da5fab6611bafb9cf89deac2cb3bb4c20e641c741e7020db4dcab553725`  
		Last Modified: Tue, 30 Aug 2022 21:38:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
