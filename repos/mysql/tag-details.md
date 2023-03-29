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
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:849a8e87076f75717e1f98102ed1545396faab1cb2c99c768bf2b5b430571604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2bbef75b058643f5a747c13661a88ee3301df9e25f0eaeb358587cc37da86afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162693934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88338e85f040d97b75f2d43518736f4af9e52fa4c4c577cd34b134273a079266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:00:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 11:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:28 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 11:00:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 11:00:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 11:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 23 Mar 2023 11:00:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:01:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:01:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:01:04 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:01:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:01:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:01:05 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:01:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac63a14e4479941312ab4b314bbd36b8eed13e848b7446b33d62d1cf387c14`  
		Last Modified: Thu, 23 Mar 2023 11:01:59 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a94b43bbfe3822fc0a3c87da156138a81cec71bf1b9a2e00f3acc1b9819eca`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 4.2 MB (4182339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38763e84573623aeb1cff67387112f2d0b31e5ed0b899e3b3a126770e46d8b94`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 1.4 MB (1441745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbc7fd4a2d7d18a737618196f4d75de0a316eaf5c125b2d4d35a7eb037426d`  
		Last Modified: Thu, 23 Mar 2023 11:01:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19764d7bd70a9eea88bec2db9d035ffe9224b9dcd7c0613e42f63b775f8f75d3`  
		Last Modified: Thu, 23 Mar 2023 11:02:00 GMT  
		Size: 14.1 MB (14086905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2769597f7f726053839c80035384b62ea02c2f3dafa473e5200c96236b67c`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55969b3a4225bf2037f3ccfc7930ed5b0cfed7aeee036deb0d7aee144dfbc425`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4898aaf83c5d2f75aa7c90e3936fb2faf0f565889f5973fb820f1330cff028`  
		Last Modified: Thu, 23 Mar 2023 11:02:10 GMT  
		Size: 115.8 MB (115832889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9972a98a4d99007516b2303bc1ca8e06d9696adff985ac28b4f52bbb086738`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8313553fddc90f14c25b3007f8f77459244ac46fbcd5580f9f3c31ba6a0d1`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:849a8e87076f75717e1f98102ed1545396faab1cb2c99c768bf2b5b430571604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2bbef75b058643f5a747c13661a88ee3301df9e25f0eaeb358587cc37da86afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162693934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88338e85f040d97b75f2d43518736f4af9e52fa4c4c577cd34b134273a079266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:00:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 11:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:28 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 11:00:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 11:00:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 11:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 23 Mar 2023 11:00:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:01:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:01:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:01:04 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:01:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:01:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:01:05 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:01:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac63a14e4479941312ab4b314bbd36b8eed13e848b7446b33d62d1cf387c14`  
		Last Modified: Thu, 23 Mar 2023 11:01:59 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a94b43bbfe3822fc0a3c87da156138a81cec71bf1b9a2e00f3acc1b9819eca`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 4.2 MB (4182339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38763e84573623aeb1cff67387112f2d0b31e5ed0b899e3b3a126770e46d8b94`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 1.4 MB (1441745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbc7fd4a2d7d18a737618196f4d75de0a316eaf5c125b2d4d35a7eb037426d`  
		Last Modified: Thu, 23 Mar 2023 11:01:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19764d7bd70a9eea88bec2db9d035ffe9224b9dcd7c0613e42f63b775f8f75d3`  
		Last Modified: Thu, 23 Mar 2023 11:02:00 GMT  
		Size: 14.1 MB (14086905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2769597f7f726053839c80035384b62ea02c2f3dafa473e5200c96236b67c`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55969b3a4225bf2037f3ccfc7930ed5b0cfed7aeee036deb0d7aee144dfbc425`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4898aaf83c5d2f75aa7c90e3936fb2faf0f565889f5973fb820f1330cff028`  
		Last Modified: Thu, 23 Mar 2023 11:02:10 GMT  
		Size: 115.8 MB (115832889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9972a98a4d99007516b2303bc1ca8e06d9696adff985ac28b4f52bbb086738`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8313553fddc90f14c25b3007f8f77459244ac46fbcd5580f9f3c31ba6a0d1`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41`

```console
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-debian`

```console
$ docker pull mysql@sha256:849a8e87076f75717e1f98102ed1545396faab1cb2c99c768bf2b5b430571604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2bbef75b058643f5a747c13661a88ee3301df9e25f0eaeb358587cc37da86afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162693934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88338e85f040d97b75f2d43518736f4af9e52fa4c4c577cd34b134273a079266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:00:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 11:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:28 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 11:00:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 11:00:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 11:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:00:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Mar 2023 11:00:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 23 Mar 2023 11:00:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:01:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:01:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:01:04 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:01:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:01:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:01:05 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:01:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac63a14e4479941312ab4b314bbd36b8eed13e848b7446b33d62d1cf387c14`  
		Last Modified: Thu, 23 Mar 2023 11:01:59 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a94b43bbfe3822fc0a3c87da156138a81cec71bf1b9a2e00f3acc1b9819eca`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 4.2 MB (4182339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38763e84573623aeb1cff67387112f2d0b31e5ed0b899e3b3a126770e46d8b94`  
		Last Modified: Thu, 23 Mar 2023 11:01:58 GMT  
		Size: 1.4 MB (1441745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbc7fd4a2d7d18a737618196f4d75de0a316eaf5c125b2d4d35a7eb037426d`  
		Last Modified: Thu, 23 Mar 2023 11:01:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19764d7bd70a9eea88bec2db9d035ffe9224b9dcd7c0613e42f63b775f8f75d3`  
		Last Modified: Thu, 23 Mar 2023 11:02:00 GMT  
		Size: 14.1 MB (14086905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2769597f7f726053839c80035384b62ea02c2f3dafa473e5200c96236b67c`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55969b3a4225bf2037f3ccfc7930ed5b0cfed7aeee036deb0d7aee144dfbc425`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4898aaf83c5d2f75aa7c90e3936fb2faf0f565889f5973fb820f1330cff028`  
		Last Modified: Thu, 23 Mar 2023 11:02:10 GMT  
		Size: 115.8 MB (115832889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9972a98a4d99007516b2303bc1ca8e06d9696adff985ac28b4f52bbb086738`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8313553fddc90f14c25b3007f8f77459244ac46fbcd5580f9f3c31ba6a0d1`  
		Last Modified: Thu, 23 Mar 2023 11:01:55 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-oracle`

```console
$ docker pull mysql@sha256:2860414595702acd275100720266beb30a21c4076b549e022105aca6e3a7c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c59226e8d38ce4f0f3f15bef7e8ff53065b48e8d5b7816341bd6c20907bedeb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130058693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea3fb7309a304def7ce3018a44b4f732de4decea4fba7e7520ff703bc5135c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:43:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:43:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:44:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:44:19 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 29 Mar 2023 00:44:20 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 29 Mar 2023 00:44:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:44:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:44:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:44:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 29 Mar 2023 00:45:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:45:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:45:02 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:45:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:45:03 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:45:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383599866d46fbae6106afe703ca2d4d91cb12b928600276e5439486a8c4fd53`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9b00d1546e2e04ce14fc1af8aed38826ee32ed3ffb162928cb2c51e100861`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 983.7 KB (983715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b533688d5bd959f5d05a8ff56cc7d7360687f12adeaa512a98d180c9f0a61d`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 4.6 MB (4580697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6edd904932a6512123c49abdccc842aa97fd3a7c9977a413e20e2d3b13576f`  
		Last Modified: Wed, 29 Mar 2023 00:45:54 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9d1dbc4ecbbbbb93ca40d2e893549afc00a31feabc440cf484b36ab6f8c65`  
		Last Modified: Wed, 29 Mar 2023 00:45:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1421081aa1a5765a007891fe373aaad07211e1e634d6e26cf6ebb014aaed7c`  
		Last Modified: Wed, 29 Mar 2023 00:45:55 GMT  
		Size: 25.5 MB (25525948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1fed27908962dc9ff6a99d9ca52a24a7b0541af341daa043b746cfef570bd`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1e715b0b24368dd7eff39287bdbfb9d535880228671b23f9e65c7861fe10f`  
		Last Modified: Wed, 29 Mar 2023 00:46:00 GMT  
		Size: 48.5 MB (48465952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8175c49cc5cd4b4ccd7a718e5e9761748015f92833413a83ddfd5df566b50a`  
		Last Modified: Wed, 29 Mar 2023 00:45:52 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda56d8df0482e6ad0e4c7880fb0ed4637f518646bd78e99c06cc511946c0c1`  
		Last Modified: Wed, 29 Mar 2023 00:45:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:01003f288c58133dad270905e2768e6a1d399d709a4a1375bc4f982f747252c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:38d6c177f28baa3b93350a59f0aae2c032418f05e2efd979c9da22d0a27d6223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8288d09e99593d17141361840c289947140d8e35f633ddeba0fab989abe3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:59:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 10:59:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:38 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 10:59:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 10:59:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 10:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 23 Mar 2023 10:59:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:00:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:00:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:00:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Mar 2023 11:00:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:00:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:00:11 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:00:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6521829aee0429164fc3f7c547e84502400c78acde7a204473309a69c42de3`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9f91eb302bb05cb9afddd1700b2642fd6618c437d04f4185f607b6328a96b4`  
		Last Modified: Thu, 23 Mar 2023 11:01:27 GMT  
		Size: 4.4 MB (4414934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13030349449a434afe037605a64bb8d3a329f038982cfc259d41614e5e07f9e6`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 1.5 MB (1471385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c2b6b8463df89c8f2a6360c2f660aeaecfc6af04623b90c8672633b45508cf`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c28230983db4101bc642c49ad9db328e79021f759b015452312fee84088bfd`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 12.7 MB (12661950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d22d367ac2dbd2c3b82ae8b262419d0f4c0d52a347e70aec590b2ea0e3706d5`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2bb5025fa157b775e71b1d4f2cdecd14b2d34b980f991ae86b50d0774057da`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e14277cdd802f47544aaa9a804c183ddef124757546b539b7c0f09379805728`  
		Last Modified: Thu, 23 Mar 2023 11:01:40 GMT  
		Size: 127.8 MB (127795886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a14127bf2fafa4308b78730e859d21a1d282b9508753a915c77fb970028891f`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed869d4966e891b12c705ddc7bb0f1f6cdb851ae2fc9106a46778f4c5f568ec7`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40298f9476557edea1f63b547f12e3a6814b8b110333bc90760d9363f86d8383`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:01003f288c58133dad270905e2768e6a1d399d709a4a1375bc4f982f747252c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:38d6c177f28baa3b93350a59f0aae2c032418f05e2efd979c9da22d0a27d6223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8288d09e99593d17141361840c289947140d8e35f633ddeba0fab989abe3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:59:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 10:59:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:38 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 10:59:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 10:59:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 10:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 23 Mar 2023 10:59:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:00:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:00:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:00:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Mar 2023 11:00:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:00:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:00:11 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:00:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6521829aee0429164fc3f7c547e84502400c78acde7a204473309a69c42de3`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9f91eb302bb05cb9afddd1700b2642fd6618c437d04f4185f607b6328a96b4`  
		Last Modified: Thu, 23 Mar 2023 11:01:27 GMT  
		Size: 4.4 MB (4414934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13030349449a434afe037605a64bb8d3a329f038982cfc259d41614e5e07f9e6`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 1.5 MB (1471385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c2b6b8463df89c8f2a6360c2f660aeaecfc6af04623b90c8672633b45508cf`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c28230983db4101bc642c49ad9db328e79021f759b015452312fee84088bfd`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 12.7 MB (12661950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d22d367ac2dbd2c3b82ae8b262419d0f4c0d52a347e70aec590b2ea0e3706d5`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2bb5025fa157b775e71b1d4f2cdecd14b2d34b980f991ae86b50d0774057da`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e14277cdd802f47544aaa9a804c183ddef124757546b539b7c0f09379805728`  
		Last Modified: Thu, 23 Mar 2023 11:01:40 GMT  
		Size: 127.8 MB (127795886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a14127bf2fafa4308b78730e859d21a1d282b9508753a915c77fb970028891f`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed869d4966e891b12c705ddc7bb0f1f6cdb851ae2fc9106a46778f4c5f568ec7`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40298f9476557edea1f63b547f12e3a6814b8b110333bc90760d9363f86d8383`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-debian`

```console
$ docker pull mysql@sha256:01003f288c58133dad270905e2768e6a1d399d709a4a1375bc4f982f747252c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.32-debian` - linux; amd64

```console
$ docker pull mysql@sha256:38d6c177f28baa3b93350a59f0aae2c032418f05e2efd979c9da22d0a27d6223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8288d09e99593d17141361840c289947140d8e35f633ddeba0fab989abe3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:59:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 10:59:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:38 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 10:59:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 10:59:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 10:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 23 Mar 2023 10:59:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:00:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:00:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:00:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Mar 2023 11:00:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:00:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:00:11 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:00:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6521829aee0429164fc3f7c547e84502400c78acde7a204473309a69c42de3`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9f91eb302bb05cb9afddd1700b2642fd6618c437d04f4185f607b6328a96b4`  
		Last Modified: Thu, 23 Mar 2023 11:01:27 GMT  
		Size: 4.4 MB (4414934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13030349449a434afe037605a64bb8d3a329f038982cfc259d41614e5e07f9e6`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 1.5 MB (1471385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c2b6b8463df89c8f2a6360c2f660aeaecfc6af04623b90c8672633b45508cf`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c28230983db4101bc642c49ad9db328e79021f759b015452312fee84088bfd`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 12.7 MB (12661950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d22d367ac2dbd2c3b82ae8b262419d0f4c0d52a347e70aec590b2ea0e3706d5`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2bb5025fa157b775e71b1d4f2cdecd14b2d34b980f991ae86b50d0774057da`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e14277cdd802f47544aaa9a804c183ddef124757546b539b7c0f09379805728`  
		Last Modified: Thu, 23 Mar 2023 11:01:40 GMT  
		Size: 127.8 MB (127795886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a14127bf2fafa4308b78730e859d21a1d282b9508753a915c77fb970028891f`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed869d4966e891b12c705ddc7bb0f1f6cdb851ae2fc9106a46778f4c5f568ec7`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40298f9476557edea1f63b547f12e3a6814b8b110333bc90760d9363f86d8383`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-oracle`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:01003f288c58133dad270905e2768e6a1d399d709a4a1375bc4f982f747252c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:38d6c177f28baa3b93350a59f0aae2c032418f05e2efd979c9da22d0a27d6223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8288d09e99593d17141361840c289947140d8e35f633ddeba0fab989abe3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:59:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Mar 2023 10:59:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:38 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Mar 2023 10:59:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Mar 2023 10:59:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Mar 2023 10:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:59:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Mar 2023 10:59:55 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Thu, 23 Mar 2023 10:59:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Mar 2023 11:00:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Mar 2023 11:00:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Mar 2023 11:00:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Mar 2023 11:00:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Mar 2023 11:00:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Mar 2023 11:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 11:00:11 GMT
EXPOSE 3306 33060
# Thu, 23 Mar 2023 11:00:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6521829aee0429164fc3f7c547e84502400c78acde7a204473309a69c42de3`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9f91eb302bb05cb9afddd1700b2642fd6618c437d04f4185f607b6328a96b4`  
		Last Modified: Thu, 23 Mar 2023 11:01:27 GMT  
		Size: 4.4 MB (4414934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13030349449a434afe037605a64bb8d3a329f038982cfc259d41614e5e07f9e6`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 1.5 MB (1471385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c2b6b8463df89c8f2a6360c2f660aeaecfc6af04623b90c8672633b45508cf`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c28230983db4101bc642c49ad9db328e79021f759b015452312fee84088bfd`  
		Last Modified: Thu, 23 Mar 2023 11:01:26 GMT  
		Size: 12.7 MB (12661950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d22d367ac2dbd2c3b82ae8b262419d0f4c0d52a347e70aec590b2ea0e3706d5`  
		Last Modified: Thu, 23 Mar 2023 11:01:24 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2bb5025fa157b775e71b1d4f2cdecd14b2d34b980f991ae86b50d0774057da`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e14277cdd802f47544aaa9a804c183ddef124757546b539b7c0f09379805728`  
		Last Modified: Thu, 23 Mar 2023 11:01:40 GMT  
		Size: 127.8 MB (127795886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a14127bf2fafa4308b78730e859d21a1d282b9508753a915c77fb970028891f`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed869d4966e891b12c705ddc7bb0f1f6cdb851ae2fc9106a46778f4c5f568ec7`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40298f9476557edea1f63b547f12e3a6814b8b110333bc90760d9363f86d8383`  
		Last Modified: Thu, 23 Mar 2023 11:01:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
