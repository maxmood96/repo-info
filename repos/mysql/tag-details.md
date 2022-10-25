<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.40`](#mysql5740)
-	[`mysql:5.7.40-debian`](#mysql5740-debian)
-	[`mysql:5.7.40-oracle`](#mysql5740-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.31`](#mysql8031)
-	[`mysql:8.0.31-debian`](#mysql8031-debian)
-	[`mysql:8.0.31-oracle`](#mysql8031-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-oracle`

```console
$ docker pull mysql@sha256:f5e2d4d7dccdc3f2a1d592bd3f0eb472b2f72f9fb942a84ff5b5cc049fe63a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:64dc581e69a2e37825c4f669c2c5903f258d8fca529632c73c5e7c8095432c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144333003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14905234a4ed471d6da5b7e09d9e9f62f4d350713e2b0e8c86652ebcbf710238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:47:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:47:51 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:48:14 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 21 Oct 2022 19:48:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 21 Oct 2022 19:48:15 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Fri, 21 Oct 2022 19:48:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:48:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:48:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:48:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Fri, 21 Oct 2022 19:48:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:49:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:49:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:49:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:49:00 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:49:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734cfb67bc8c9872bd458b7c82e7bc3eca010f38a4ccac07d863814eee2f1b07`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729529a0299eeb95c68e8bfdbc237b671d751e84bfc592bca377c27cf1e31161`  
		Last Modified: Fri, 21 Oct 2022 19:50:22 GMT  
		Size: 930.2 KB (930221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d3c603a591da29f582821512adaf4197fe52d1aa3ac42491aad2128955d8b4`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 4.5 MB (4546654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e0fbc2dcba0e8cb13b1616914d09abacc8e4147bf12a3b5ceca138092304e`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 2.7 KB (2661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d48a00fea276947ad91562783d98ed45ab5e77fa93552cd0a3ef3a46804d4`  
		Last Modified: Fri, 21 Oct 2022 19:50:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf883b19c2f3cff48bacc06c394c73797b49be19dbebeda4580ed88da02bf8f`  
		Last Modified: Fri, 21 Oct 2022 19:50:21 GMT  
		Size: 25.5 MB (25530033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28356e1795930ab9e9381e3865ad898ca95634fc19e4425e1ae28afcd3c49412`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abbf373312d0ae94e6305d1eb72750dce128536fd6856d127c48e61aa19086`  
		Last Modified: Fri, 21 Oct 2022 19:50:29 GMT  
		Size: 63.5 MB (63460272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6621986fd3a5a82e124a82937242e3f839efa4e051f4cb9925e50ee46806a`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d631e923a6f3a6ed2683dbbeda6ad90723ead236157f68e506999448fd6685`  
		Last Modified: Fri, 21 Oct 2022 19:50:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.31-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-oracle`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:06314a7a220f6043436cfd72fd9c7f174fd58ef69fe4b788625fa53be4ab66aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fe2a93f68a7ddef56a39cbc8b3faaf41ca6c910978255119941c1b71899aa6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157264983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad08b3c84be3e9164f86153224ab616bf71ee2c79677154c2e5cd3179cccfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:46:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 19:46:11 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 19:46:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 19:46:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:46:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 19:46:38 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:46:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 19:47:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 19:47:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 19:47:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 19:47:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 19:47:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 19:47:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 19:47:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 19:47:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 19:47:45 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 19:47:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca853f7184003ce4a998ddf789288fb6bca33039a73cbd4ba03ba525f27bb7`  
		Last Modified: Fri, 21 Oct 2022 19:49:41 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a20476962308f364c624cd515a836f813023b7bff68e93ae6aeac715b0e8f21`  
		Last Modified: Fri, 21 Oct 2022 19:49:42 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fea56f9fb03595109612dc70a638e205294bcdda1964e39dd3851ee949fff`  
		Last Modified: Fri, 21 Oct 2022 19:49:40 GMT  
		Size: 4.6 MB (4607033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058249d3104921cd4d5c5885643a97a8be8f9a69124fc9beed35cf791a0813f`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5014a20163fa346756c80c1114d1ea993e9478cdfb6c08da61684a56b3e2af`  
		Last Modified: Fri, 21 Oct 2022 19:49:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aa7388ee2006b8f4362b5e9e068081be6bfc44a8f3b2bcddd6921cf7d54c7`  
		Last Modified: Fri, 21 Oct 2022 19:49:46 GMT  
		Size: 56.0 MB (56046468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5e2150967eeafa4e4e92254de9f529ea591d2d4b32ac6bf879b2cdb510222`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6b15dcdf4eda4c5061aefe4f754f90946717295e7fa5ea7dbaccff2b4f368f`  
		Last Modified: Fri, 21 Oct 2022 19:49:48 GMT  
		Size: 55.1 MB (55084220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de4337b977fd518044876a04543776db696d6bc40559290e2dc785f3fa1cd2`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dab154f2aeb6b8b6a8282f9df9d12aea07b392a14b82d9f9d04003f9588863`  
		Last Modified: Fri, 21 Oct 2022 19:49:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5dae1c4fb603384ad5f68d3a792e5cc1095c23740785261740f00d0739e097b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155562941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d53e5f7cab773dc36cea9ba5009d948dbffd06acceb29c4ffed2f75f4ad51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 20:02:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 21 Oct 2022 20:02:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 21 Oct 2022 20:02:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 21 Oct 2022 20:02:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 21 Oct 2022 20:02:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 21 Oct 2022 20:02:44 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 21 Oct 2022 20:02:45 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:02:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 21 Oct 2022 20:03:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 21 Oct 2022 20:03:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 21 Oct 2022 20:03:20 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Fri, 21 Oct 2022 20:03:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 21 Oct 2022 20:03:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 21 Oct 2022 20:03:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 21 Oct 2022 20:03:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 21 Oct 2022 20:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Oct 2022 20:03:57 GMT
EXPOSE 3306 33060
# Fri, 21 Oct 2022 20:03:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f573f3d8f30de658c99546dfd56922e80e9293938b142d28198865c4c4a9ac`  
		Last Modified: Fri, 21 Oct 2022 20:04:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4de9dcca6a477790d74ccaf1a44e93d82058c1abfe8acc7d9949cd166f40e03`  
		Last Modified: Fri, 21 Oct 2022 20:04:34 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3d1d1f0399c6049042613a98e9c464de870d057f8589f496ad644fca5baad8`  
		Last Modified: Fri, 21 Oct 2022 20:04:32 GMT  
		Size: 4.4 MB (4433279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283bc354d9b803601a6cfc1b2c93b8497c0eca55ca6c4180663c547784192ce9`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2e77bf45616b4d382065d9adcf89ae082529714fb253e1672aed550a3d166`  
		Last Modified: Fri, 21 Oct 2022 20:04:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d13a94caf14e2d057950a534f5c7bb6e3ea40449ac98341a77d3de764270b6`  
		Last Modified: Fri, 21 Oct 2022 20:04:37 GMT  
		Size: 55.4 MB (55421386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c1f1629008ad09afd71e6e8ac0337985cf8bb01382d50dfcbad35efa1789cb`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f892d0f3ede917e6800f61a5c88869e6897dd7a85dd6664d864f9a17b5757c64`  
		Last Modified: Fri, 21 Oct 2022 20:04:39 GMT  
		Size: 55.4 MB (55433315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b88d5e2639641c57de86ca6641db6b00fdb7908b52bbfce8d5c2809b78039`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f0dbf65c702dbec59a92b1a9238a7cdc44967a4d67908b9153a401781bf11`  
		Last Modified: Fri, 21 Oct 2022 20:04:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
