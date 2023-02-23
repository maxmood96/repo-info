<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.41`](#mysql5741)
-	[`mysql:5.7.41-debian`](#mysql5741-debian)
-	[`mysql:5.7.41-oracle`](#mysql5741-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.32`](#mysql8032)
-	[`mysql:8.0.32-debian`](#mysql8032-debian)
-	[`mysql:8.0.32-oracle`](#mysql8032-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:6476de3ab220f0c20f01d7d730c019988ec68a82e993f578dafc1a3b94895fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b6dc77221a0b35c7aa40f4cc1e284c119d6ad33f12c9a0526164142217336462
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f99a3d9960fe8b2191dfa28727117aa725c2075afd787cfb02a69ec0bf88e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:26:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:27:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:27:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:27:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 09 Feb 2023 10:27:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:27:28 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:27:28 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:27:28 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:27:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:27:29 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:27:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32964b27b18a9ee810264517aca8110893e509b330e12acdbabb0975acec9cf4`  
		Last Modified: Thu, 09 Feb 2023 10:28:36 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cb395a9ad2806c234c69205fb53c2285af2123149583db57d29cda565922c6`  
		Last Modified: Thu, 09 Feb 2023 10:28:35 GMT  
		Size: 4.2 MB (4182329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a15ae9a5ff8db2b3cccd825da0959ad97e9311c7663ee2f099615dc781998`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 1.4 MB (1441767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4750b84b045a6e1a710e75bd26ec9047126c079dcdcb1f7422f28effed77adbd`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c585ef195068cd6a1da8f2c3ae3ac9610098c7a1a1979ea49cb55a77cbc57a5`  
		Last Modified: Thu, 09 Feb 2023 10:28:37 GMT  
		Size: 14.1 MB (14089423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226c572bc1e666f11e709fea2c27b2f3bb017430c15f5aef0e6d579ad70c1b54`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d69ec5a2f74b7e950bdbb989d92ea7d3f801c4e7234305d280ee560161af5`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3a0b1a65202d1cafb287fb738ced57cbf69568854e8a495916472c8bfb76d`  
		Last Modified: Thu, 09 Feb 2023 10:28:48 GMT  
		Size: 115.8 MB (115832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681eb1ae9d85d3e3b4581b8eae20c8cfc147b0c018ec0836272ec80f23a4ff93`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841305cd41e20dfdf326d7fec6ab8a2b9dc69a9bca203c0230dc197905adc0e7`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:6476de3ab220f0c20f01d7d730c019988ec68a82e993f578dafc1a3b94895fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b6dc77221a0b35c7aa40f4cc1e284c119d6ad33f12c9a0526164142217336462
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f99a3d9960fe8b2191dfa28727117aa725c2075afd787cfb02a69ec0bf88e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:26:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:27:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:27:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:27:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 09 Feb 2023 10:27:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:27:28 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:27:28 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:27:28 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:27:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:27:29 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:27:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32964b27b18a9ee810264517aca8110893e509b330e12acdbabb0975acec9cf4`  
		Last Modified: Thu, 09 Feb 2023 10:28:36 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cb395a9ad2806c234c69205fb53c2285af2123149583db57d29cda565922c6`  
		Last Modified: Thu, 09 Feb 2023 10:28:35 GMT  
		Size: 4.2 MB (4182329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a15ae9a5ff8db2b3cccd825da0959ad97e9311c7663ee2f099615dc781998`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 1.4 MB (1441767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4750b84b045a6e1a710e75bd26ec9047126c079dcdcb1f7422f28effed77adbd`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c585ef195068cd6a1da8f2c3ae3ac9610098c7a1a1979ea49cb55a77cbc57a5`  
		Last Modified: Thu, 09 Feb 2023 10:28:37 GMT  
		Size: 14.1 MB (14089423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226c572bc1e666f11e709fea2c27b2f3bb017430c15f5aef0e6d579ad70c1b54`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d69ec5a2f74b7e950bdbb989d92ea7d3f801c4e7234305d280ee560161af5`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3a0b1a65202d1cafb287fb738ced57cbf69568854e8a495916472c8bfb76d`  
		Last Modified: Thu, 09 Feb 2023 10:28:48 GMT  
		Size: 115.8 MB (115832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681eb1ae9d85d3e3b4581b8eae20c8cfc147b0c018ec0836272ec80f23a4ff93`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841305cd41e20dfdf326d7fec6ab8a2b9dc69a9bca203c0230dc197905adc0e7`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-debian`

```console
$ docker pull mysql@sha256:6476de3ab220f0c20f01d7d730c019988ec68a82e993f578dafc1a3b94895fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b6dc77221a0b35c7aa40f4cc1e284c119d6ad33f12c9a0526164142217336462
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f99a3d9960fe8b2191dfa28727117aa725c2075afd787cfb02a69ec0bf88e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:26:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:27:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:27:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:27:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 09 Feb 2023 10:27:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:27:28 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:27:28 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:27:28 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:27:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:27:29 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:27:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32964b27b18a9ee810264517aca8110893e509b330e12acdbabb0975acec9cf4`  
		Last Modified: Thu, 09 Feb 2023 10:28:36 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cb395a9ad2806c234c69205fb53c2285af2123149583db57d29cda565922c6`  
		Last Modified: Thu, 09 Feb 2023 10:28:35 GMT  
		Size: 4.2 MB (4182329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a15ae9a5ff8db2b3cccd825da0959ad97e9311c7663ee2f099615dc781998`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 1.4 MB (1441767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4750b84b045a6e1a710e75bd26ec9047126c079dcdcb1f7422f28effed77adbd`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c585ef195068cd6a1da8f2c3ae3ac9610098c7a1a1979ea49cb55a77cbc57a5`  
		Last Modified: Thu, 09 Feb 2023 10:28:37 GMT  
		Size: 14.1 MB (14089423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226c572bc1e666f11e709fea2c27b2f3bb017430c15f5aef0e6d579ad70c1b54`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d69ec5a2f74b7e950bdbb989d92ea7d3f801c4e7234305d280ee560161af5`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3a0b1a65202d1cafb287fb738ced57cbf69568854e8a495916472c8bfb76d`  
		Last Modified: Thu, 09 Feb 2023 10:28:48 GMT  
		Size: 115.8 MB (115832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681eb1ae9d85d3e3b4581b8eae20c8cfc147b0c018ec0836272ec80f23a4ff93`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841305cd41e20dfdf326d7fec6ab8a2b9dc69a9bca203c0230dc197905adc0e7`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:a5a6abbcea1c4980cd26159a141e76e6b61c7bb4bd646c451e2de427ac109e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:285a51d29dcd451bb19e8ea95ccdc3821623b479d4c4ac9502f7d8f7bb97770e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee0d5c0bb6c6cba6e891921672f9db100ebb8de2cd4756a25534f5355d742d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:25:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:26:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:26:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 09 Feb 2023 10:26:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:26:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:26:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:26:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 09 Feb 2023 10:26:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:26:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:26:37 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:26:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7b95728f21c63976c276ca6f9698c7c3bf6930ebce75f7e4e8beb60a98321`  
		Last Modified: Thu, 09 Feb 2023 10:28:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2431a387ba17c6e7d4ef50e5c7bd6e47629b95792dded824c3566f3476c428`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 4.4 MB (4414977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f58cbce0349eb0706ae41c8f34c0955cc74f5cb4d9b0cb086682647b51ad87`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 1.5 MB (1471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15447575be2a06f415c246f6060f8deb4b88876c9b0329c571c3a06678da08a1`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fb8835dfec3abac8a936eb08eec9afdc5f4edd39a801d07b3954e659879dd5`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 12.7 MB (12661942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda3df60cab197cb15b81a3da99ef596ae56fbe45ddfa11650c6abe3c0940ff`  
		Last Modified: Thu, 09 Feb 2023 10:27:58 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06690264afdf54515ea7068b7360a33492348b29356423ae0e9eed4ae864fa0`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31600770994e9b6b4057d325e15ec90db2d58a23222325600628798e05db9961`  
		Last Modified: Thu, 09 Feb 2023 10:28:16 GMT  
		Size: 127.8 MB (127795730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b2d3594118f5bdf0a1ce6add2e43506e888b8497eecd7601976cd3e9ac90f`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c7fa7652204a4ffee2cd5c11f585ddaa77004c0d20986521aea43345d01192`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fda57e156ba0b60c0ca6cfbd16eb91fd9c3a8b1ad6d0ef6121631c0354a5d8`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:a5a6abbcea1c4980cd26159a141e76e6b61c7bb4bd646c451e2de427ac109e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:285a51d29dcd451bb19e8ea95ccdc3821623b479d4c4ac9502f7d8f7bb97770e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee0d5c0bb6c6cba6e891921672f9db100ebb8de2cd4756a25534f5355d742d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:25:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:26:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:26:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 09 Feb 2023 10:26:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:26:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:26:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:26:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 09 Feb 2023 10:26:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:26:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:26:37 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:26:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7b95728f21c63976c276ca6f9698c7c3bf6930ebce75f7e4e8beb60a98321`  
		Last Modified: Thu, 09 Feb 2023 10:28:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2431a387ba17c6e7d4ef50e5c7bd6e47629b95792dded824c3566f3476c428`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 4.4 MB (4414977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f58cbce0349eb0706ae41c8f34c0955cc74f5cb4d9b0cb086682647b51ad87`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 1.5 MB (1471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15447575be2a06f415c246f6060f8deb4b88876c9b0329c571c3a06678da08a1`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fb8835dfec3abac8a936eb08eec9afdc5f4edd39a801d07b3954e659879dd5`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 12.7 MB (12661942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda3df60cab197cb15b81a3da99ef596ae56fbe45ddfa11650c6abe3c0940ff`  
		Last Modified: Thu, 09 Feb 2023 10:27:58 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06690264afdf54515ea7068b7360a33492348b29356423ae0e9eed4ae864fa0`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31600770994e9b6b4057d325e15ec90db2d58a23222325600628798e05db9961`  
		Last Modified: Thu, 09 Feb 2023 10:28:16 GMT  
		Size: 127.8 MB (127795730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b2d3594118f5bdf0a1ce6add2e43506e888b8497eecd7601976cd3e9ac90f`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c7fa7652204a4ffee2cd5c11f585ddaa77004c0d20986521aea43345d01192`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fda57e156ba0b60c0ca6cfbd16eb91fd9c3a8b1ad6d0ef6121631c0354a5d8`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-debian`

```console
$ docker pull mysql@sha256:a5a6abbcea1c4980cd26159a141e76e6b61c7bb4bd646c451e2de427ac109e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.32-debian` - linux; amd64

```console
$ docker pull mysql@sha256:285a51d29dcd451bb19e8ea95ccdc3821623b479d4c4ac9502f7d8f7bb97770e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee0d5c0bb6c6cba6e891921672f9db100ebb8de2cd4756a25534f5355d742d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:25:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:26:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:26:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 09 Feb 2023 10:26:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:26:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:26:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:26:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 09 Feb 2023 10:26:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:26:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:26:37 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:26:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7b95728f21c63976c276ca6f9698c7c3bf6930ebce75f7e4e8beb60a98321`  
		Last Modified: Thu, 09 Feb 2023 10:28:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2431a387ba17c6e7d4ef50e5c7bd6e47629b95792dded824c3566f3476c428`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 4.4 MB (4414977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f58cbce0349eb0706ae41c8f34c0955cc74f5cb4d9b0cb086682647b51ad87`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 1.5 MB (1471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15447575be2a06f415c246f6060f8deb4b88876c9b0329c571c3a06678da08a1`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fb8835dfec3abac8a936eb08eec9afdc5f4edd39a801d07b3954e659879dd5`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 12.7 MB (12661942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda3df60cab197cb15b81a3da99ef596ae56fbe45ddfa11650c6abe3c0940ff`  
		Last Modified: Thu, 09 Feb 2023 10:27:58 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06690264afdf54515ea7068b7360a33492348b29356423ae0e9eed4ae864fa0`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31600770994e9b6b4057d325e15ec90db2d58a23222325600628798e05db9961`  
		Last Modified: Thu, 09 Feb 2023 10:28:16 GMT  
		Size: 127.8 MB (127795730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b2d3594118f5bdf0a1ce6add2e43506e888b8497eecd7601976cd3e9ac90f`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c7fa7652204a4ffee2cd5c11f585ddaa77004c0d20986521aea43345d01192`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fda57e156ba0b60c0ca6cfbd16eb91fd9c3a8b1ad6d0ef6121631c0354a5d8`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-oracle`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:a5a6abbcea1c4980cd26159a141e76e6b61c7bb4bd646c451e2de427ac109e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:285a51d29dcd451bb19e8ea95ccdc3821623b479d4c4ac9502f7d8f7bb97770e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee0d5c0bb6c6cba6e891921672f9db100ebb8de2cd4756a25534f5355d742d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:25:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:26:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:26:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 09 Feb 2023 10:26:19 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 09 Feb 2023 10:26:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:26:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:26:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:26:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 09 Feb 2023 10:26:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:26:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:26:37 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:26:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7b95728f21c63976c276ca6f9698c7c3bf6930ebce75f7e4e8beb60a98321`  
		Last Modified: Thu, 09 Feb 2023 10:28:00 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2431a387ba17c6e7d4ef50e5c7bd6e47629b95792dded824c3566f3476c428`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 4.4 MB (4414977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f58cbce0349eb0706ae41c8f34c0955cc74f5cb4d9b0cb086682647b51ad87`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 1.5 MB (1471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15447575be2a06f415c246f6060f8deb4b88876c9b0329c571c3a06678da08a1`  
		Last Modified: Thu, 09 Feb 2023 10:27:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fb8835dfec3abac8a936eb08eec9afdc5f4edd39a801d07b3954e659879dd5`  
		Last Modified: Thu, 09 Feb 2023 10:28:01 GMT  
		Size: 12.7 MB (12661942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda3df60cab197cb15b81a3da99ef596ae56fbe45ddfa11650c6abe3c0940ff`  
		Last Modified: Thu, 09 Feb 2023 10:27:58 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06690264afdf54515ea7068b7360a33492348b29356423ae0e9eed4ae864fa0`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31600770994e9b6b4057d325e15ec90db2d58a23222325600628798e05db9961`  
		Last Modified: Thu, 09 Feb 2023 10:28:16 GMT  
		Size: 127.8 MB (127795730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b2d3594118f5bdf0a1ce6add2e43506e888b8497eecd7601976cd3e9ac90f`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c7fa7652204a4ffee2cd5c11f585ddaa77004c0d20986521aea43345d01192`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fda57e156ba0b60c0ca6cfbd16eb91fd9c3a8b1ad6d0ef6121631c0354a5d8`  
		Last Modified: Thu, 09 Feb 2023 10:27:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
